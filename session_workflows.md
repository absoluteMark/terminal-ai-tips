# Session Start and End Workflows with AI Agents

This document outlines a specific use case for using AI agents to automate session start and session end workflows. The goal is to streamline the process of setting up your development environment and saving your progress.

## Session Start Workflow

The goal of the session start workflow is to quickly and efficiently set up the development environment, ensuring that the AI has the necessary context to begin working on a task.

### Steps

1.  **User Initiates the Session:** The user starts the session with a specific goal or task in mind.

    **Example Prompt:**
    > "Good morning! I want to continue working on the user authentication feature. Please get me up to speed."

2.  **AI Agent Gathers Context:** The AI agent reads the relevant context files to understand the current state of the project. This may include:
    *   `gemini.md`: A file containing general project information for the Gemini model.
    *   `claude.md`: A file containing general project information for the Claude model.
    *   `project_structure.txt`: A file containing the output of the `tree` command.
    *   Other relevant files, such as the main entry point of the application or the files that were modified in the previous session.

3.  **AI Agent Asks Clarifying Questions:** The AI agent may ask clarifying questions to ensure it understands the task.

    **Example AI Response:**
    > "Good morning! I see that you were working on the `auth.js` file and had just finished implementing the login function. The next step in the plan was to add password hashing. Is that what you would like to work on now?"

4.  **AI Agent Proposes a Plan of Action:** Once the AI agent understands the task, it proposes a plan of action.

    **Example AI Response:**
    > "Okay, I will now open the `auth.js` file and add the `bcrypt` library for password hashing. I will then modify the `register` function to hash the user's password before saving it to the database. Does that sound correct?"

## Session End Workflow

The goal of the session end workflow is to save the progress, update the context files, and commit the changes to a Git repository.

### Steps

1.  **User Signals the End of the Session:** The user tells the AI agent that they are finished with the current work session.

    **Example Prompt:**
    > "I'm done for the day. Please wrap things up for me."

2.  **AI Agent Updates Context Files:** The AI agent updates the context files with any new information or changes. This may include:
    *   Updating the project structure file if new files were created.
    *   Adding notes about the current state of the project to the `gemini.md` or `claude.md` files.

3.  **AI Agent Stages Changed Files:** The AI agent stages the changed files in Git.

    **Example AI Action:**
    ```bash
    git add .
    ```

4.  **AI Agent Generates a Commit Message:** The AI agent generates a descriptive commit message that summarizes the changes made during the session.

    **Example AI Response:**
    > "I have staged the following files: `auth.js`, `package.json`, and `package-lock.json`. I will now generate a commit message. How does this sound: 'feat(auth): implement password hashing using bcrypt'?"

5.  **AI Agent Commits the Changes:** After the user approves the commit message, the AI agent commits the changes.

    **Example AI Action:**
    ```bash
    git commit -m "feat(auth): implement password hashing using bcrypt"
    ```

6.  **(Optional) AI Agent Pushes Changes:** The user can also instruct the AI agent to push the changes to a remote repository.

    **Example Prompt:**
    > "Looks good. Please push the changes to the `develop` branch."

    **Example AI Action:**
    ```bash
    git push origin develop
    ```
