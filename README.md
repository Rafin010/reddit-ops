# Reddit Operations

A practical Make custom app starter for **Reddit subreddits and posts**. This repository is designed for import and continued development in the Make Apps Editor or Apps SDK workflow.

## What it provides

The app includes a reusable basic-token connection, a **Get resource** action, a **Search resources** module, a **Make an API call** universal module, and an RPC starter for dynamic resource loading. The endpoint defaults to `https://oauth.reddit.com` and can be overridden in the connection settings when the service uses a tenant-specific host.

## Repository layout

| Path | Purpose |
| --- | --- |
| `makecomapp.json` | Make custom app manifest and component map |
| `connection/` | Connection parameters and authenticated request behavior |
| `modules/` | Module parameters, communication, output schema, and samples |
| `rpcs/` | Dynamic dropdown/resource loading starter |
| `base.iml.json` | Shared IML configuration |

## Setup

Create a Custom App in Make Developer Hub, then import or copy the files from this repository into the Apps Editor. Add the service API key or access token in the connection, set the correct base URL, and test the modules against a sandbox account before production use. Never commit credentials; the `.gitignore` file excludes `.secrets/`.

## Extending the app

Replace the generic resource paths with the service's documented endpoints, refine `parameters.json` for required fields, and update `expect.json` and `samples.json` with the exact response shape. Add webhook components only after confirming that the service supports the desired callback event.

## Validation

Run the following command to confirm that the manifest is valid JSON:

```bash
npm run validate
```

## Disclaimer

This is an independent community starter and is not affiliated with or endorsed by Reddit Operations. Review the service API terms, authentication requirements, rate limits, and licensing before publishing.

## References

- [Make Custom Apps Documentation](https://developers.make.com/custom-apps-documentation)
- [Make Modules Documentation](https://developers.make.com/custom-apps-documentation/app-components/modules.md)
- [Make Connections Documentation](https://developers.make.com/custom-apps-documentation/app-components/connections.md)
