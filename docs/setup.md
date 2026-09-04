# Setup

## Demo Mode

1. In n8n, choose **Import → From file** and select the workflow JSON.
2. Keep the workflow inactive.
3. Click **Execute workflow**.
4. Open **Human Review Packet** and inspect the metrics, evidence references, brief, and review flags.

Demo Mode requires no credentials and uses the fictional AegisLayer dataset embedded in the Code node. The copy in `demo-data/` is provided for inspection and offline fixture work.

## API Mode

Configure `MELTWATER_API_BASE_URL`, `MELTWATER_API_TOKEN`, and `MELTWATER_SAVED_SEARCH_ID` using the deployment's environment or an approved n8n credential. Set `input_mode` to `MELTWATER_API`, then test with a non-sensitive saved search. Confirm the response is an array or contains `mentions`, `data`, or `results` before relying on the normalizer.

Do not enable the workflow or connect outbound communication nodes without a separate review of access, retention, and publishing controls.
