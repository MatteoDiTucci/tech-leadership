# Page data

## Problem
In a single page application, a page fetches data from different external systems.  
Adding new functionalities to the page gets harder because the unit tests are increasingly complex around faking external systems.  
This happens because unit tests are coupled to the internals of how data are fetched and transformed.

## Context
- The page is a Next.js server side component
- External systems are for instance: content management system (CMS) and product service
- The external systems are queried multiple times, for instance: fetch different components from the CMS
- Page unit tests are written in react-testing-library, test framework is Vitest
- Mocking capabilities are provided by Vitest
- When page unit tests fail, it is very difficult to understand what Vitest mock needs to be fixed

## Solution
Extract all the page data fetching and transformation into a single `getPageData()` function.
Now we can:
- Unit test `getPageData()` without the complexity of the UI (just Vitest, no react-testing-library)
- Unit test the page by only faking `getPageData()`

### GetPageData function
An example of such function can be:
```
export const getHomePageData = (locale: Locale) => {
    const homePageContent = cmsClient().getHomePage() 
    const footer = cmsClient().getFooter() 
    const productRecommendations = productService().getReccomendations() 
    
    return {
        footer,
        heroImage: homePageContent.heroImage,
        productRecommendations,
        title: homePageContent.title
    }
} 
```

Unit tests for `getPageData()` will fake `cmsClient()` and `productService()`.
Page unit test will only fake `getPageData()`.

### Single responsibility
The responsibility of fetching and transforming data is extracted into `getPageData()`.   
This means the page can go back to its main responsibility: presentation through components composition.

## Notes

### Back-end for front-end
The `getPageData()` function can be thought as a tiny back-end-for-front-end.  
Each page has its own `getPageData()`, for instance: `getHomePageData()`, `getProductListPageData()`, etc.
