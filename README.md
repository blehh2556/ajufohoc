# How to publish your Resume Using Markdown, Github and Pelican

## Statement of Purpose
This document serves as a comprehensive guide for you, Marvin McLaren, to help you publish a resume as a static website using tools like Markdown (a lightweight markup language), Pelican(a static site generator) and GitHub(a forge). 

By following these instructions, you will learn to separate your content (the resume) from its presentation (the website), ensuring your professional data is secure, portable, and easily updated.

### Pre-Requisites
To successfully publish your resume on the web, you will need: 
1. A computer that uses a **Windows 10** system and above. 

2. A **GitHub** Account-  Create one with this [Link](https://github.com/signup)

3. **Visual Studio Code** - install [here](https://code.visualstudio.com/download). Click the *"Windows"* button.

4. **Git for Windows** - install [here](https://git-scm.com/install/windows)

5. **Python 3.10+** - Install [here](https://git-scm.com/install/windows). **CRITICAL**: Check the box "Add Python to PATH" during installation.

6. **Github Desktop** - Install [here](https://desktop.github.com/download/).

7. **Background Knowledge**: Familiarity with the concepts in Andrew Etter's book, Modern Technical Writing, specifically regarding static generators, markdown and forges.


## Section 1: Creating and Syncing your repository 

Before we begin to write markdown code, we need to create a structure that will hold all our work. In this section, we will create a GitHub repository and link it to a folder on our computer in a way that will allow us to sync local changes with those on GitHub web.

**Part A: Create the GitHub Repository**

1. Log in to your GitHub account.

2. Click the "+" icon in the top-right corner. 

3. Select "New repository" from the dropdown menu.

4. Name your repository (e.g., ajufohoc).

5. Navigate to choose visibility. 

6. Set visibility to Public. (This is so Pelican can access it later).

7. Check the box that says *"Add a README file."* 

8. Click "Create repository."

**Part B: Connecting your online repository to your local machine**

After completing part A, you have created a new repository. On the screen, you should see a single README file. Now that the "cloud" version exists, we need to bring it down to your computer.

1. Sign into the same Github account on Github Desktop.

2. Select **File** in the top left corner. 

3. Select **Clone Repository**

4. Select the repository you created in part A from the list.  

5. Click **choose** under "Local Path."

6. Navigate to **This PC > Windows (C:)**.

7. Press **clone**.

*Result: GitHub Desktop will create a folder on your computer that is "twinned" with the website.*


## Section 2: Formatting Your Resume in Markdown

Now that your tech is set up, you can draft your resume. Following Etter’s advice, we use Markdown to define what the information is (a header, a list, a link) rather than how it looks (font size, colour, margins). We also opt for Markdown over Microsoft Word because like Etter explains, it gets complicated to deploy websites using Word, as word and pdf aren't as effective for multiple changes and living documentation. 

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

    *An important note is to be consistent with your heading sizes for each section. If you have an Education section with Heading Level 2 , your work experience should also be level 2*

5.  Press ` Ctrl + Shift + V` in VS Code. This opens a split-screen preview so you can see your formatting in real-time.

6. Save your work regularly. 

7. Press the blue **commit to main** button in the GitHub Desktop app to update the changes you've made so far.

8. Cick the blue button that says **push to origin** on the right-hand side of the page, to send it to GitHub.

    **Note**: As you make changes to your file, Andrew Etter recommends you push to your forge(GitHub) frequently. This is helpful if you need to go back to previous versions or encounter errors. 

## Section 3: Setting up a Virtual Environment 
Before we can work with Python and Pelican, we need to set up a virtual environment using these steps: 

1. Open Command Prompt. 

2. Type: `cd C:\yourFolderName` 

3. Type in this code:<br>`python -m venv .venv `

4. Press Enter.

5. Type in this code:<br> `.venv\Scripts\activate ` 

6. Press Enter.

    After steps 1-5, you will know you're successful if `(.venv)` is now in front of your directory. E.g:  <br>` (.venv) C:\Users\chiny>`

    Now your virtual environment is set up. Do not exit your command prompt window and proceed to the next section.

## Section 4: Setting Up Pelican

To transform your text into a website, you need an engine. We will use Python. Python allows us to run the Pelican generator, which handles all the heavy lifting of web design for you, allowing you to turn simple lightweight markup language to a website, just like Andrew Etter advised. 

1. Type in this code to install pelican and markdown in command prompt:<br> ` python -m pip install "pelican[markdown]"`

2. Type the command ` pelican-quickstart` 

3. Press Enter.

4. Follow the prompts on the screen. Press the Enter key to pick the default selections. 

    At the end of this process, Pelican has now created several folders, including one called **content**

3. Move your **Resume.md** file into the new **content** folder in your file Explorer. 


## Section 5: Publishing your Webpage

Now that Pelican is set up we can publish our webpage.

1. Type `pelican content` 

2. Press Enter.

    If you have set up correctly, you should see a message that starts with `Done: Processed 1 article` 

3. Type the command `pip install ghp-import`.

4. Press Enter.

5. Type this command `python -m ghp_import output -b gh-pages`.

6. Press Enter.

7. Type this command `git push origin gh-pages`. 

8. Press Enter.

9. **ctrl + Click** on the link generated in the command prompt output to view your repository.

10. Click the hyperlink on the right hand side called **"github-pages** under deployment.  

11. Click on the first link and it will take you to your live resume webpage ! 

## Conclusion

Congratulations Marvin! Through this process, you have transitioned from a traditional document creator to a modern technical communicator by mastering the "Docs-as-Code" workflow. You learned to implement Andrew Etter’s core principles by using Lightweight Markup (Markdown) to decouple content from design, ensuring your professional data is portable and clean. By utilising Pelican, you have moved away from complex, dynamic site builders toward a Static Site approach that prioritises security and speed. Most importantly, you learned to use a Forge (GitHub) as a safety net, adopting distributed version control to ensure your work is up-to-date, protected, and easily discoverable on the web. 

**You can explore more resources on the topic below:**

1. Learn more about the Github-flavoured Markdown Andrew Etter briefly mentioned in his book, [here](https://github.github.com/gfm/).

2. Watch this [tutorial](https://www.youtube.com/watch?v=_PPWWRV6gbA) for more clarity on Markdown.

3. Learn more about GitHub and how to manage repositories [here](https://learn.github.com/skills).

4. Learn about this other Lightweight Markup Language, [Ascii](https://docs.asciidoctor.org/asciidoc/latest/).

5. Learn how to use Rsync with this [video](https://youtu.be/Pygr_TpZRpM?si=-xrqRa7-zi5ce6vr).


## Frequently Asked Questions 

**Q: Why is Markdown Better than writing raw HTML?**

A: Andrew Etter argues that Lightweight Markup is Superior using an example of Ascii and DocBox. The DockBox content is challenging to read with human eyes because of the amount of syntax involved. The same situation applies to HTML and Markdown. Markdown is better than writing raw HTML because Markdown is easier to read in raw form compared to HTML. This makes it easier for people to contribute to documentation, Etter informs us that this leads to richer, higher quality documentation.

**Q: I changed the Markdown version of my resume, so why don't I see the changes when I refresh the website in my browser?**

A: This happens because even though you've updated the file on your computer, you haven't told Pelican to implement these changes in your output files. To see the changes, you must redo the steps in section 5 of this README.

### Credits

- Chinyere Ajufoh-Obi  

- Chika Ngene - Peer Reviewer

- Paul Watuwa - Peer Reviewer

- Andrew Etter, *Modern Technical Writing*