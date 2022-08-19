const core = require("@actions/core");
const github = require("@actions/github")
async function run() {
try {
const [owner, repo] = process.env.GITHUB_REPOSITORY.split("/");
const token = core.getinput("repo-token");
const issue = github.contex.payload.issue.number;
const octokit = new github.GitHub(token);

const label = ["new"]
//label issue
const response = await octokit.issues.addlabls({
owner,
repo,
issue_number: issue,
lables: label
});
} catch (error) {
core.setFailed(error.message);
}
}
run();
