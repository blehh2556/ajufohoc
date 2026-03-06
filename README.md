# How to publish your Resume Using Markdown, Github and Pelican

## Statement of Purpose
This document serves as a comprehensive guide for you, Marvin McLaren, to help you publish a resume as a static website using tools like Markdown (a lightweight markup language), Pelican(a static site generator) and Github(a forge). 

By following these instructions, you will learn to separate your content (the resume) from its presentation (the website), ensuring your professional data is secure, portable, and easily updated.

### Pre-Requisites
To successfully publish your resume on the web you will need: 
1. A computer that uses a **Windows 10** system and above. 

2. A **Github** Account-  Create one with this link[Link](https://github.com/signup)

3. **Visual Studio Code** - install [here](https://code.visualstudio.com/download). Make sure to click on the button that says *Windows*.

4. **Git for Windows** - install [here](https://git-scm.com/install/windows)

5. **Python 3.10+** - Install [here](https://git-scm.com/install/windows). **CRITICAL** Check the box "Add Python to PATH" during installation.

6. **Github Desktop** - Install [here](https://desktop.github.com/download/).

7. **Background Knowledge**: Familiarity with the concepts in Andrew Etter's book, Modern Technical Writing, specifically regarding static generators, markdown and forges.


## Section 1: Creating and Syncing your repository 

Before we begin to write markdown code we need to create a structure that will hold all our work. In this section we will create a github repository and link it to a folder on our computer in a way that will allow us to sync local changes with those on our forge on the web.

**Part A: Create the Github Repository**

1. Log in to your GitHub account.

2. Click the "+" icon in the top-right corner. 

3. select "New repository" from the dropdown menu.

4. Name your repository (e.g., ajufohoc).

5. Navigate to choose visibility and set it to Public. This is so Pelican can access it later.

6. Check the box that says *"Add a README file."* 

7. Scroll down and click "Create repository."

**Part B: Connecting your online repository to your local machine**

After completing part A you have created a new repository on the screen you should see a single README file. Now that the "cloud" version exists, we need to bring it down to your computer.

1. Sign into the same Github account on Github Desktop.

2. Select **File** In the top left corner. 

3. Select **Clone Repository**

4. Select the repository you created from part A from the list.  

5. Click **choose** under "Local Path."

6.  Navigate to **This PC > Windows (C:)**.

7. Press **clone**.

*Result: GitHub Desktop will create a folder on your computer that is "twinned" with the website.*


## Section 2: Formatting Your Resume in Markdown

Now that your tech stack is ready, you can draft your resume. Following Etter’s advice, we use Markdown to define what the information is (a header, a list, a link) rather than how it looks (font size, color, margins). We also opt for Markdown over Microsoft word because like Etter explains it gets complicated to deploy websites using Word and word and pdf aren't effective for multiple changes. 

1. Open VS Code. 

2. Open the project folder you created in Section 1.

3. Create a new File called **Resume.md**

3. Type the code below at the very top of your resume.md file:

    ```
    Title: Professional Resume
    Date: 2026-03-05
    Save_as: index.html`
    ```

    *The code above is Metadata. Think of Metadata as the "ID Badge" for your file. It helps Pelican turn your Resume from a file to a website.*

4. Type in your Resume using the necessary markdown formatting guides on this [Page](https://www.markdownguide.org/basic-syntax/) 

    *An important note is to be consistent with your heading sizes for each section. If you have an Education section with Heading Level 2 , Your work experience should also be level 2*

5.  Press ` Ctrl + Shift + V` in VS Code. This opens a split-screen preview so you can see your formatting in real-time.

6. Save your work regularly. 

7. Press the blue **commit to main** button in the Github Desktop app to update the changes you've made so far. .

8. Cick the blue button that says **push to origin** on the right hand side of the page, to send it to github.

    **Note**: As you make changes, Andrew Etter recommends you push to your forge frequently to help you catch problems.

## Section 3: Setting up a Virtual Environment 
But before we can work with Python and Pelican we need to set up a virtual environment using these steps: 

1. Open Command Prompt. 

2. Type: `cd C:\yourFolderName` 

3. Type in this code and press enter :<br>`python -m venv .venv `

4. Type in this code and press enter :<br> `.venv\Scripts\activate ` 

    After steps 1-4, you will know you're successful if `(.venv)` is now in front of your directory like this <br>` (.venv) C:\Users\chiny>`

    Now your virtual environment is set up. Do not exit your command prompt window and proceed to the next steps. 

## Section 4: Setting Up Pelican

To transform your text into a website, you need an engine. We will use Python. Python allows us to run the Pelican generator, which handles all the heavy lifting of web design for you, allowing you to turn simple lightweight markup language to a website. 

1. Type in this code to install pelican and markdown in command prompt:<br> ` python -m pip install "pelican[markdown]"`

2. Run the command ` pelican-quickstart` and follow the prompts on the screen. Press the Enter key to pick the default selections. 

    Pelican has now created  several folders including one called **content**

3. Move your **Resume.md** file into the new **content** folder in file Explorer. 


## Section 5: Publishing your Webpage

Now that Pelican is set up we can publish our webpage

1. Type `pelican content` and press enter.

    If you have set up correctly you should see a message that starts with `Done: Processed 1 article` 

2. Type the command `pip install ghp-import` and press enter.

3. Type this command `python -m ghp_import output -b gh-pages` and press enter.

4. Type this command `git push origin gh-pages` and press enter.

5. **ctrl + Click** on the link generated in the command prompt output to view your repository.

6. Click the hyperlink on the right hand side called **"github-pages** under deployment.  

7. Click on the first link and it will take you to your live resume webpage ! 

## Conclusion

Congratulations Marvin! Through this process, you have transitioned from a traditional document creator to a modern technical communicator by mastering the "Docs-as-Code" workflow. You learned to implement Andrew Etter’s core principles by using Lightweight Markup (Markdown) to decouple content from design, ensuring your professional data is portable and clean. By utilizing Pelican, you have moved away from complex, dynamic site builders toward a Static Site approach that prioritizes security and speed. Most importantly, you learned to use a Forge (GitHub) as a  safety net, adopting distributed version control to ensure your work is up-to-date, protected, and easily discoverable on the web. 

**You can explore more resources on the topic below:**

1. Learn more about the Github flavoured Markdown Andrew Etter briefly mentioned in his book, [here](https://github.github.com/gfm/#list-items).

2. Learn more about github and how to manage repositories [here](https://learn.github.com/skills).

3. Learn about this other lightweight markup language, [Ascii](https://docs.asciidoctor.org/asciidoc/latest/).

4. Learn how to use Rsync with this [video](https://youtu.be/Pygr_TpZRpM?si=-xrqRa7-zi5ce6vr).


## Frequently Asked Questions 

**Q: Why is Markdown Better than writing raw HTML?**


A: Markdown is better than writing raw HTML because Markdown is easier to read in raw form compared to HTML. This makes it easier for people to understand and contribute to documentation.

**Q: I changed the Markdown version of my resume, so why don't I see the canges when I refresh the website in my browser?**

A: This happens because even though you've updated the file locally you haven't told Pelican to implement these changes in your output files. To see the changes you must re-do the steps in section 5 oof this README.

### Credits

- Chinyere Ajufoh-Obi - Author 

- Chika Ngene - Class Groupmate