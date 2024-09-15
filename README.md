# Triggering the Workflow via REST API
You can trigger the workflow with a REST API call as follows:

```bash
curl -X POST \
  -H "Accept: application/vnd.github+json" \
  -H "Authorization: Bearer YOUR_GITHUB_TOKEN" \
  https://api.github.com/repos/lucianoayres/github-actions-test/actions/workflows/YOUR_WORKFLOW_FILENAME/dispatches \
  -d '{"ref":"main", "inputs": {"model": "YOUR_MODEL_NAME", "prompt": "YOUR_PROMPT"}}'
```

- Replace YOUR_GITHUB_TOKEN with your personal access token.
  - The token must have the ACTION and WORKFLOW permission with READ and WRITE permissions 
- Replace YOUR_WORKFLOW_FILENAME.yml with the name of the workflow file (for example, query-ollama-v-4-1.yml).
- Set "YOUR_MODEL_NAME" to the model you want to run (e.g., llama3.1).
- - Set "YOUR_PROMPT" to the model you want to run (e.g., Explain me LLMs like I'm five).
