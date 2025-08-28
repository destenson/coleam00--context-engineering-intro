# Claude Code Commands

Claude Code commands allow you to interact with the codebase in a more intuitive way. You can use these commands to perform various tasks, such as searching for code snippets, generating new code, and refactoring existing code.

## My Workflow

Essentially, Claude hallucinates every word it outputs. So, context is king.

Claude will often make "bad decisions" (it literally doesn't know what it's doing) but given good context, and iteration, it can produce quite impressive results. I've seen it one-shot a task that would have taken hours of coding, testing, and iteration to do manually.

Primary commands I use:
- `/generate-prp "filename (opt)" "description, facts, links, or other instructions"`
- `/execute-prp "filename (opt)"`
- `/update-todo`
- `/update-readme`
- `/review-codebase`

The rest of the commands remain largely untested and may give unexpected results.
- `/add-tests`
- `/analyze-performance`
- `/analyze-prps`
- `/api-design`
- `/audit-tech-debt`
- `/cleanup`
- `/code-review`
- `/fix-bug`
- `/fix-compile-error`
- `/generate-docs`
- `/refactor`
- `/security-audit`
- `/ui-design`

### Greenfield project

Note: As of Claude Code vX.Y, the following workflow is recommended for new projects.

Note: As of Claude Code vX.Y, I don't recommend compressing context when it gets low. I try to tell claude to wrap up its task, record its progress in a file, and "we'll continue tomorrow".

- Start with a simple `README.md` with a high-level description of the project.
  - The readme should include the purpose of the project, its features, and requirements.
  - The readme can be as simple as a few sentences or as detailed as a full page.
  -
- Create a `TODO.md` file to track tasks and features.
  - The todo file should include a list of tasks, their status (e.g., TODO, IN PROGRESS, DONE), and any relevant notes or links.
  - It can start empty, or with a few initial tasks.
  -
- Create a `PLANNING.md` file to outline the architecture and design decisions.
  - The planning file should include the overall architecture, key components, and any design patterns or principles being followed.
  - It can also include links to relevant resources or documentation.
  -
- Eventually, run `/init` in claude code to scan the codebase and generate a `CLAUDE.md` file.
- Run `/generate-prp "Initial description of the project, with any specific requirements or constraints, documentation links, or need-to-know information"` to create the first PRP files.
  - The PRP files will outline the specific features and tasks to be completed, along with any relevant details or requirements.
  - The PRP files will be used to guide the development process and ensure that all necessary tasks are completed.
  - 
- Use `/execute-prp "filename"` to implement the features outlined in the PRP files.
  - If /review-codebase had run previously, the filename is not necessary.
- Run `/update-todo`
- Run `/review-codebase` to review the changes made by the PRP files & prepare for the next run. It tends to assume that everything it just wrote is perfect, so be sure to review the changes carefully.

When I notice that Claude has made a mistake or missed something, I can provide feedback (while its still running) and/or try again. This iterative process helps improve the quality of the output. If it goes wildly off track, it may be a good idea to stop the process and start over (potentially reverting changes first).

If you run out of context, I recommend exiting the current session and starting a new one.
After starting a new session, don't run `/update-todo`, or `/review-codebase` until after you run the last command again, e.g. `/execute-prp`, to proceed.
