1. My dad has a small business in the gun industry. The majority advertisement platforms don't like the gun industry, but some social media platforms like youtube do allow videos that talk about the gun industry to some degree. YouTube policies don't allow links to sites that sell guns, but it looks like they do allow talking about your gun selling company name and what your company does. So the plan is to make an AI tool that can create and post social media content (mainly youtube videos for now) that talks about my dad's company so that he can get the company name out there without using paid advertisements.

2. Since this tool is not even a start up company but just a product, there needs to be zero or near-zero operational costs AKA no overhead. So currently planning to make the tool as a desktop app with no backend server except to validate the key for using the product. So that means we will need to find a solution like wasm to run logic natively for any logic that needs to be speedy. The plan for languages currently is vue 3 and golang or python.
```mermaid
graph TD;
    UI/client-->key verification server;
    UI/client-->ChatGPT's API;
    UI/client-->Youtube's API;
    UI/client-->Other Social Media APIs;
```