# Day-46-Reusable-Workflows-Composite-Actions

## Challenge Tasks

## Task 1: Understand workflow_call

Before writing any code, research and answer in your notes:

  1. What is a reusable workflow?

    -A reusable workflow is a GitHub Actions workflow that you can reuse in other workflows instead of writing the same code again.
     
  2. What is the workflow_call trigger?

    - workflow_call is a special trigger that allows a workflow to be called by another workflow.
     
   3. How is calling a reusable workflow different from using a regular action (uses:)?
      
      - Action = small task 
      - Reusable workflow = full pipeline

   4. Where must a reusable workflow file live?
      
      -.github/workflows/


## Task 2: Create Your First Reusable Workflow

Create .github/workflows/reusable-build.yml:

   1. Set the trigger to workflow_call
   2. Add an inputs: section with:

   - app_name (string, required)
   - environment (string, required, default: staging)

 3. Add a secrets: section with:
    - docker_token (required)
 4. Create a job that:
       - Checks out the code
       - Prints Building <app_name> for <environment>
        - Prints Docker token is set: true (never print the actual secret)
