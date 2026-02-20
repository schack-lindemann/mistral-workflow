# Frequently Asked Questions (FAQ)

### How do I set up an alternative AI model?

The workflow is now configured for Mistral AI's LeChat. You can change the API endpoints and model names in the [Workflow Environment Variables](https://www.alfredapp.com/help/workflows/advanced/variables/#environment). This requires advanced configuration and is not something we can provide support for, but [our community can help you].

### How do I access the service behind a proxy?

Add a new https_proxy key in [Workflow Environment Variables](https://www.alfredapp.com/help/workflows/advanced/variables/#environment). Or configure the proxy for all workflows under Alfred Preferences → Advanced → Network.

### Why can’t I use the workflow with a LeChat Plus subscription?

[The LeChat API and LeChat Plus subscription are billed separately.](https://docs.mistral.ai/api)

### How can I reuse pre-made prompts?

Make a new workflow with a [Keyword Input](https://www.alfredapp.com/help/workflows/inputs/keyword/) and connect it to an [Arg and Vars Utility](https://www.alfredapp.com/help/workflows/utilities/argument/) with your custom prompt text plus `{query}`, which will be replaced with new input from the Keyword. Then connect it to a [Call External Trigger Output](https://www.alfredapp.com/help/workflows/outputs/call-external-trigger/) set to open `continue_chat` from this workflow.


### Why does nothing happen when I run the workflow?

Something always happens, so check the [debugger](https://www.alfredapp.com/help/workflows/advanced/debugger/). Ensure you [installed the Automation Tasks](https://www.alfredapp.com/help/kb/automation-task-not-found/).

### How do I report an issue?

Accurate and thorough information is crucial for a proper diagnosis. **At a minimum, your report should include:**

* The [debugger](https://www.alfredapp.com/help/workflows/advanced/debugger/) output of the failing action.
* Your installed versions of: the Workflow, Alfred, and macOS. *Be precise, don’t say “latest”.*

### Why do I keep getting Quota exceeded?

You need API credits to use the workflow. You can [view your remaining credits and top up your account on the Mistral website](https://admin.mistral.ai/organization/billing).

### Why do I keep getting `[Connection Stalled]`?

This happens when the workflow takes too long to receive a reply from the API. Try increasing the timeout in the [Workflow’s Configuration](https://www.alfredapp.com/help/workflows/user-configuration/). If the problem persists, it indicates a problem either with your connection or Mistral’s service.
