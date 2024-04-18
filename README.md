# Github Action Notes

It devided into three main steps: workflows, jobs and steps. We can have multiple workflows as we want.<br>
Workflows: Attached to a github repository, contain one or more jobs, trigered upon events.<br>
Jobs: Define a runner (execution env), Contain one or more steps, run in parallel or sequential, can be conditional.<br>
Steps: Execute a shell script or action, can be custom or thirdparty actions, Steps are axecuted in order, can be conditional.<br>

#### Github action is free for public repositories and some minutes is free for private repositories.
You can add github action in your projects by adding .github/workflows folder. Inside this folder, you can add your yml files.<br>
You can visit: https://github.com/marketplace to find third party actions.<br>
We can use official github action commands for our use: https://github.com/marketplace/actions/checkout