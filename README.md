
# How to publish your Resume Using Markdown, Github and Pelican

## Statement of Purpose
This document serves as a comprehensive guide for you, Marvin McLaren, to help you publish a resume as a static website using tools like Markdown(a lightweight markup language), Pelican(a static site generator) and Github(a forge). 

By following these intructions, you will learn to separate your content (the resume) from its presentation (the website), ensuring your professional data is secure, portable, and easily updated.

### Pre-Requisites
To successfully host your resume you need: 
1. A computer that uses a **Windows 10** system and above. 

2. A **Github** Account-  Create one with this link[Link](https://github.com/signup)

3. **Visual Studio Code** - install [here](https://code.visualstudio.com/download). Make sure to click on the button that says *Windows*.

4. **Git for Windows** - install [here](https://git-scm.com/install/windows)

5. **Python 3.10+** - Install [here](https://git-scm.com/install/windows). **CRITICAL** Check the box "Add Python to PATH" during installation.

6. **Github Desktop** - Install [here](https://desktop.github.com/download/).

7. **Background Knowledge**: Familiarity with the concepts in Andrew Etter's book, Modern Technical Writing, specifically regarding static generators, markdown and forges.


## Section 1: Creating and Syncing your repository 

Before we begin to write markdown code we need to create a structure that will hold all our work. In this section we will create a folder on our computer and link that to our github repository in a way that will allow us to sync local changes with those on the web in github.

**Part A: Create the Github Repository**

1. Log in to your GitHub account.

2. Click the "+" icon in the top-right corner and select "New repository."

3. Name your repository (e.g., ajufohoc).

4. Navigate to choose visibility and set it to Public. This is so Pelican can access it later.

5. Check the box that says *"Add a README file."* 

6. Scroll down and click "Create repository."

**Part B: Connecting your online repository to your local machine**

After completing part A you have created a new repository on the screen you should see a single README file. Now that the "cloud" version exists, we need to bring it down to your computer.

1. Open Github Desktop and sign in to the same Github account.

2. In the top left corner select File > Clone repository.

3. Select the repository you created from part A from the list.  

4. Under "Local Path," click Choose. Navigate to This PC > Windows (C:).

5. Press clone.

*Result: GitHub Desktop will create a folder on your computer that is "twinned" with the website.*


## Section 2: Formatting Your Resume in Markdown

Now that your tech stack is ready, you can draft your resume. Following Etter’s advice, we use Markdown to define what the information is (a header, a list, a link) rather than how it looks (font size, color, margins). We also opt for Markdown over Microsoft word because like Etter explains it gets complicated to deploy websites using Word.

1. Open VS Code: Launch the app and open the project folder you created in Phase 1.

2. Create a new File call it **Resume.md**

3. Think of Metadata as the "ID Badge" for your file. It helps Pelican turn your Resume from a file to a website. 

At the very top of your resume.md file type this:
<pre><code>
Title: Professional Resume
Date: 2026-03-05
Save_as: index.html`
</code></pre>


4. Type in your work experience using the necessary markdown formatting guides on this [Page](https://www.markdownguide.org/basic-syntax/) 

5. An important note is to be consistent with your heading sizes for each section. if you have an Education section with Heading Level 2 , Your work experience should also be level 2

6. Preview Your Work: Press ` Ctrl + Shift + V` in VS Code. This opens a split-screen preview so you can see your formatting in real-time.

7. After saving in markdown, push your work to the forge by going into Github desktop and committing any changes to main.

8. On the right hand side click the blue button that says **push to origin** to send it to github online.

## Section 3: Setting up a Virtual Environment 
But before we can work with Python and Pelican we need to set up a virtual environment using these steps: 

1. Open Command Prompt. 

2.Type: `cd C:\yourFolderName` 

3. Type in this code and press enter :<br>`python -m venv .venv `

4. Next, type in this code and press enter :<br> `.venv\Scripts\activate ` 

5. You will know you're successful if `(.venv)` is now infront of your directory like this <br>` (.venv) C:\Users\chiny>`

6. Now your virtual environment is set up. Do not exit your command prompt window and proceed to the next steps. 

## Section 4: Setting Up Pelican

To transform your text into a website, you need an engine. We will use Python. Python allows us to run the Pelican generator, which handles all the heavy lifting of web design for you. 

1. In your opened command prompt type in this code to install oelican and markdown :<br> ` python -m pip install "pelican[markdown]"`

2. Next run the command ` pelican-quickstart` and follow the prompts. 

3. Pelican has now created  several folders includeinf one called **content**

4. In your file Explorer move your **Resume.md** file into the new **content** folder. 


## Section 5: Publishing your Webpage

1. Build the site: Type `pelican content`

    If you have set up correctly you should see a message that starts with `Done: Processed 1 article` 

2. Next Run the command `pip install ghp-import`

3. Then `python -m ghp_import output -b gh-pages`

4. And finally, `git push origin gh-pages`

5. **ctrl + Click** on the link generated in the command prompt output to view your repository. (You can also view this via Github.com)

6. On the right hand side you should see **"github-pages** under deployment. Click that link. 

7. On this page, click on the first link and it will take you to your live resume webpage ! 

## Conclusion

Congratulations Marvin! Through this process, you have transitioned from a traditional document creator to a modern technical communicator by mastering the "Docs-as-Code" workflow. You learned to implement Andrew Etter’s core principles by using Lightweight Markup (Markdown) to decouple content from design, ensuring your professional data is portable and clean. By utilizing Pelican, you has moved away from complex, dynamic site builders toward a Static Site approach that prioritizes security and speed. Most importantly, you learned to use a Forge (GitHub) as a professional safety net, adopting Distributed Version Control to ensure your work is versioned, protected, and easily "discoverable". 

**You can explore more resources on the topic below:**

### Frequently Asked Questions 

**Q: Why is Markdown Better than writing raw HTML?**

A: According to Andrew Etter in his book *Modern Technical Writing*, you should use Markdown 

**Q: Why is Markdown Better than writing raw HTML?**


### Credits

- Chinyere Ajufoh-Obi - Author 

- Chika Ngele - Class Groupmate