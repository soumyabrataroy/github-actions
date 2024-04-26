# Github Action Notes

It devided into three main steps: workflows, jobs and steps. We can have multiple workflows as we want.<br>
Workflows: Attached to a github repository, contain one or more jobs, trigered upon events.<br>
Jobs: Define a runner (execution env), Contain one or more steps, run in parallel or sequential, can be conditional.<br>
Steps: Execute a shell script or action, can be custom or thirdparty actions, Steps are axecuted in order, can be conditional.<br>

#### Github action is free for public repositories and some minutes is free for private repositories.
You can add github action in your projects by adding .github/workflows folder. Inside this folder, you can add your yml files.<br>
You can visit: https://github.com/marketplace to find third party actions.<br>
We can use official github action commands for our use: https://github.com/marketplace/actions/checkout

We can use 
run: |
    echo "First output"
    echo "Second output"
to execute multiple echo commands.

#### Run a project using Github actions
To run a project, we need to create one folder called .github/workflows and yml file inside the workflows folder.
<br>
To trigger a workflow, we can use different events like push, pull etc. You can find more about it here: https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows
<br>
Here action is specifically more complex commands developed by third party vendors. You can see them here: https://github.com/marketplace/actions/checkout
<br>
The official action from github team is the checkout action.
<br>
If you use 'run' command - it will use run on github actions. e.g. run echo "print something"<br>
If you use 'uses' command - it will uses action command on github. uses actions/checkout@v3
<br>
We can run multiple actions in parallel (default). We need to indent properly and it will run the jobs. We can also run jobs sequencially. In that case , we need to add 'need: previous job name' to run the jobs sequentially.
<br>
We can also add multiple events to trigger the workflow. In that case we need mention the triggers inside the square bracket. 
[push, workflow_dispatchs] 
<br>
We can also access some information using github expression feature. We will be using the data using reserved keywords like ${{github}} etc. <br>
You can learn more about github expressions here: https://docs.github.com/en/actions/learn-github-actions/expressions
