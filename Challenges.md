# Project Challeges
Throughout the project many simple and complex problems came up, so in the case that anyone wants to use this project as a framework or wanting to go further and modify thinks he or she should have the following in mind. 

## Wikipedia API
The dept of search, the number of links per page can make a big difference not only in time to complete but also in the dept and width of concentrated knowledge. Too shallow and few links the knowledgebase remains unknowledgeable, too deep and before you know it spans multiple fields losing its focus and risking garbage query results. If it is for a specialized RAG you will probably want an excellent coverage of the subject without out of context articles. Giving a wide and diverse initial page selection can help massively. 

By default, when retrieving links from a page the API returns their results in an alphabetic order. If having a limiter in small page you will miss half the alphabet if you are lucky and in larger pages might get results only starting with “A”.

In Wikipedia many articles have cyclical connections, so you need a filter both for optimizing your crawl and for securing the quality and diversity of results. Also, a filter helps with image links, issn, empty pages, e.t.c.

Lastly in general Articles starting with “List of…” tend to be lacking real information but for a RAG, in this case in art, have a use if you want to tackle questions like where there is grouping with similar characteristics like ethnicity, century, art movement, e.t.c”  


## Splitting
No matter the splitting there is always the risk of a small chunk with very little information as they lack context and because of the small number of words tend to be selected by the queries if they have the same word or phrase and so block the useful chunks from been used. So a filter by chunk size to make sure that all chunks are usable is very helpful.

The chunk size is very important as you might expect although I suspected that a larger size would bring better results, a smaller size (500) and overlap of 10% (50) was found through testing to be the ideal combination. The only drawback was the larger number of chunks and so the execution time. 

Here is a tip when you are content with your vector database save it for later.  

## LLMs
Both Claude 3 and GPT3.5 Turbo were incredible and easy to work with. But I preferred the OpenAI API for being cheaper (a lot cheaper) and giving slightly more natural responses. Moreover, as you might expect the same prompt gave different output in each model and each had to be calibrated individually. Also, Claude tends to be more theatrical with its character but always started its response the same way, not very natural, so I had to suppress it a lot. 

Also, small LLM that could run on collab like “flan-t5” were unable to get the prompt and used it as a response. So either run a larger model locally on a beefy machine or server or use an API and avoid the hustle if you don’t want to get your hands dirty.  

