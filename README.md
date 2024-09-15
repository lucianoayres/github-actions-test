Triggering the Workflow via REST API:
You can trigger the workflow with a REST API call as follows:

```bash
curl -X POST \
  -H "Accept: application/vnd.github+json" \
  -H "Authorization: Bearer YOUR_GITHUB_TOKEN" \
  https://api.github.com/repos/lucianoayres/github-actions-test/actions/workflows/YOUR_WORKFLOW_FILENAME.yml/dispatches \
  -d '{"ref":"main", "inputs": {"model": "your-model-name"}}'
```

- Replace YOUR_GITHUB_TOKEN with your personal access token.
- Replace YOUR_WORKFLOW_FILENAME.yml with the name of the workflow file (for example, install-run-ollama.yml).
- Set "your-model-name" to the model you want to run (e.g., llama3.1).
