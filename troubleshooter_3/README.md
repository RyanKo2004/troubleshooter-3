# NOC troubleshooter
A troubleshooting agent powered by claude that helps junior engineers at the NOC solve networking issues.

## prerequisites

- **Visual Studio Code**: To download click this link and follow the instructions https://code.visualstudio.com/download


- **claude code**: To download click this link and follow the instructions https://code.visualstudio.com/download Do note that you will need an active anthropic account and an Anthropic API key

## getting started

### 1. Create Your Workspace

- **Use this repository as a template:**
  1. Click **"Use this template"** on the GitHub page.
  2. Create a new repository from the template.
  3. Clone your new repository:
     ```
     git clone https://github.com/your-username/your-new-repo.git
     ```

### 2. Open in VS Code

- Launch VS Code.
- Open your cloned workspace folder.

## workflow guide

### 1. set up
- ensure you are in this directory
- perform the command 'claude' in the terminal
- once claude is open, perform the command 'read system_instructions.md

### 2. how to use
- simply type your issue into claude and await response
- note that responses will explicitly state the workflow used



## Core Files and Their Purposes

- CLI references: folder that holds the CLI references of the many vendors used
- Issues: folder that holds all the issues that can't be resolved by a junior engineer
- SOPS: folder that holds all the workflows 
- issues_template.md: file that contains the template used to create issues
- system_instructions.md: The crux of this whole project. This file is used to program a custom troubleshooting agent using all the resources available to it

## current functionality
- able to guide junior engineers through a simple troubleshooting problem 
- follows the CLI_references and workflows as closely as possible
- If workflows don't cover the problem, web search is allowed to be used

## next steps
- increase the scope of workflows available by using API calls through bookstacks. This requires higher security clearance
- Improve UI so that it is easier to use
- eventually can be used by senior engineers in more difficult and complex problems


