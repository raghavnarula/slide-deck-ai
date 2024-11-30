---
title: SlideDeck AI
emoji: 🏢
colorFrom: yellow
colorTo: green
sdk: streamlit
sdk_version: 1.32.2
app_file: app.py
pinned: false
license: mit
---

# SlideDeck AI

We spend a lot of time on creating the slides and organizing our thoughts for any presentation. 
With SlideDeck AI, co-create slide decks on any topic with Generative Artificial Intelligence.
Describe your topic and let SlideDeck AI generate a PowerPoint slide deck for you—it's as simple as that!

SlideDeck AI is powered by [Mistral-Nemo-Instruct-2407](https://huggingface.co/mistralai/Mistral-Nemo-Instruct-2407).


# Process

SlideDeck AI works in the following way:

1. Given a topic description, it uses Mistral Nemo Instruct to generate the *initial* content of the slides. 
The output is generated as structured JSON data based on a pre-defined schema.
2. Next, it uses the keywords from the JSON output to search and download a few images with a certain probability.
3. Subsequently, it uses the `python-pptx` library to generate the slides, 
based on the JSON data from the previous step. 
A user can choose from a set of three pre-defined presentation templates.
4. At this stage onward, a user can provide additional instructions to *refine* the content.
For example, one can ask to add another slide or modify an existing slide.
A history of instructions is maintained.
5. Every time SlideDeck AI generates a PowerPoint presentation, a download button is provided.
Clicking on the button will download the file.


# Icons

SlideDeck AI uses a subset of icons from [bootstrap-icons-1.11.3](https://github.com/twbs/icons)
 (MIT license) in the slides. A few icons from [SVG Repo](https://www.svgrepo.com/)
(CC0, MIT, and Apache licenses) are also used. 



# Local Development

SlideDeck AI uses [Mistral-Nemo-Instruct-2407](https://huggingface.co/mistralai/Mistral-Nemo-Instruct-2407) 
via the Hugging Face Inference API.
To run this project by yourself, you need to provide the `HUGGINGFACEHUB_API_TOKEN` API key,
for example, in a `.env` file. For image search, the `PEXEL_API_KEY` should be added. 
Visit the respective websites to obtain the keys.
