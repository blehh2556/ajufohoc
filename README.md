
# How to publish your Resume Using Markdown, Github and Pelican

## Statement of Purpose
This document serves as a comprehensive guide for you, Marvin McLaren, to help you publish a resume as a static website using tools like Markdown(a lightweight markup language), Pelican(a static site generator) and Github(a forge). 

By following these intructions, you will learn to separate your content (the resume) from its presentation (the website), ensuring your professional data is secure, portable, and easily updated.

### Pre-Requisites
To successfully host your resume you need: 
1. A computer that uses a **Windows 10** system and above. 
2. A **Github** Account-  you can create an account or log in using this [Link](https://github.com/signup)
3. **Visual Studio Code** - you can install the app with this [Link](https://code.visualstudio.com/download). Make sure to click on the button that says *Windows*.
4. **Git installed** - you can install it by following the prompts at this [Link](https://git-scm.com/install/windows)
5. **Python 3.10+** - you can install it by following the prompts at this [Link](https://git-scm.com/install/windows)
6. **Familiarity** with lightweight markup languages, distributed version control systems, statig generators and a forge via **Andrew Etter's** book, *Modern Technical Writing*



## Section 1: Setting up your Project Structure

Before we begin to write markdown code we need to create a structure that will hold all our work. 

1. Open File explorer and go to your root directory in 

## Section 2: Formatting Your Resume in Markdown
**NEED AN ETTER PRACTICAL PRINCIPLE - ASSIGNMENT 

## Section 3: Setting aVirtual Environment 
But before we can work with Python and Pelican we need to set up a virtual environment using these steps: 

1. Open Command Prompt. This is your terminal** Your directory should look similar to this `C:\Users\chiny> `
2. Type in this code and press enter :<br>`python -m venv .venv `
3. Next, type in this code and press enter :<br> `.venv\Scripts\activate ` 
4. You will know you're successful if `(.venv)` is now infront of your directory like this <br>` (.venv) C:\Users\chiny>`
5. Now your virtual environment is set up. Do not exit your command prompt window and proceed to the next steps. 

## Section 4: Setting Up Pelican

To transform your text into a website, you need an engine. We will use Python. Python allows us to run the Pelican generator, which handles all the heavy lifting of web design for you. 

Since Python is already installed on your computer and we have set up your virtual environment we can proceed with using Pelican:

1. In your opened command prompt type in this code to install oelican and markdown :<br> ` python -m pip install "pelican[markdown]"
`
2.  use pelican set up in slides 


## Section 5: Publishing your Webpage


Pushing to github 
Install that thing 
Then 

will ask for git authentication when you 



In a traditional word processor, if you save over a file or a document gets corrupted, that work may be lost forever. However, by using GitHub, every time you "push" an update to your resume, the Forge creates a permanent snapshot of that version. If you make a mistake or don't like a formatting change, you can instantly retrieve a previous version. This ensures that your professional documentation is secure, versioned, and publicly accessible from any browser in the world.


Credit 
Peter Vu helped me trouble shoot virtual environments and pelican for windows 
