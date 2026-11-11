AI-aided pair:


Md Janib Rijbi, k12249462  
Markus Ennsberger-Kranabiter, k01455904



            
## Reflection on my AI-usage:  
(by markus)

I was very satisfied with the custom-generated input data created by GEMINI. Nevertheless, I hadn't a clear plan in the beginning, what I want to visualize and how. 
This resulted in a clumsy data structure and actually in too much unnecessary input data. That caused a waste in computing power. 
I think, if I had thought about my goal, used a piece of paper and a pencil instead of GEMINI I would have done a better job and tackled the solution better. 
(read more about the data generation in: How input data was generated.txt)  

For the visualization, I relied only on GEMINI. I am very satisfied with the visualization, especially because I have no clue about html programming. 
I had to repeatedly describe GEMINI what I wanted and it gradually improved it to my idealized imagination. So I needed several prompts. But this behavior is understandable, 
since I gave incomplete descriptions. Sometimes unintentionally but most of the time I thought GEMINI will deduce my wishes, which it didn't. 
I knew that those big LLMs are powerful, but I didn't actually expect, that it can do interactive visualizations during the chat also.
On the meta level, I really hate such code generation. It is impressive but I really like to understand "my" applications or visualizations. 
Because if problems come further down in the pipeline, I am even more helpless.
What I struggled the most was to get my Horizon output data into a data format that is appropriate for the visualization. But this was my fault, because I stored the 
outputs of my model in a stupid data structure to begin with. That was because I didn't think about visualization.
(read more about the visualization in: How the visualization was created and harmonized with data the data structure.txt)  

### Overall insight: 

It certainly would have helped me to be more sophisticated in visualization- and html-stuff, because then i could have written the prompts more clearly and
effectively. Because the better I know a topic the better I can provide clear instructions. In general, I got much unnecessary output from GEMINI, because 
I prompted sloppy and ambiguously.
To build something effectively (with AI), it certainly helps to be knowledgeable in this topic. But as my lack in html knowledge shows, it is not necessary. 

Also for a small task like this one it is advantageous to have a smart "architecture" that smartly shatters the task into many small ones. GEMINI can handle 
those small ones pretty well. But to design a smart architecture it is again necessary to have knowledge about the problem and also know the corresponding 
technical terms. Only then we can give useful prompts and use GenAi effectively. So finally, LLMs aren't an excuse to avoid becoming knowledgeable about 
programming—or anything else.



## Reflection on my AI-usage:  
(by md janib)

For my part (political opinions) I used Claude to set up the experiment in Google Colab and to create the plots. I was very satisfied with how fast I got a working notebook. 
Especially the attention visualization would have taken me much longer without AI.

Nevertheless, the generated code did not work perfectly from the beginning. I had to run it myself, check the results and give feedback, so it took several prompts 
until everything worked. Some problems were only setup issues, like the Hugging Face token or the access to the Gemma model. 
A more important problem was with K2-Horizon: the answers were first read wrong from the model output. I only noticed this because I looked at the raw answers of the model. 
After fixing it, the results made much more sense. This showed me that I can't just trust the final plots.
Like Markus, I also think it is a disadvantage when you don't fully understand "your" code. If something goes wrong, you depend on the AI again to fix it.
(read more about my AI interactions in: ai-interactions/md_janib_rijbi_claude.md)

### Overall insight: 

GenAI is very helpful to build something quickly, but you still have to check the results yourself. The better I understood the task, the clearer my prompts 
became and the better the answers were. So I agree with Markus: AI is a great tool, but it is not an excuse to avoid learning the topic yourself.
