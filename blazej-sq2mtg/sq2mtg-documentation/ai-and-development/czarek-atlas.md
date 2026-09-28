# Czarek / Atlas

## Repository status

* Repository: `SQ2MTG/czarek`
* Visibility: private
* Language: Python
* Default branch: `main`
* Description: **Private assistant by Atlas**
* Created in August 2026.
* No public license is declared.

## Architecture

Czarek is documented as a private/local AI assistant with a split architecture:

* Linux host acting as the local orchestration/client side;
* separate Windows GPU machine for model inference;
* private network/VPN connectivity between hosts;
* provider abstraction for model backends;
* routing/orchestration layer;
* embeddings and RAG;
* speech input/output and wake-word processing.

The architecture is intended to keep sensitive assistant data and infrastructure inside the user's private environment.

## AI pipeline

The project documentation identifies the following functional layers:

1. speech input / wake-word;
2. assistant request routing;
3. model-provider selection;
4. retrieval and embeddings;
5. local model inference;
6. speech synthesis/output.

This should be treated as the documented architecture rather than a claim that every component is currently production-ready.

## Security boundary

Because the repository is private and the assistant may connect to local infrastructure:

* keep API keys, VPN credentials, model credentials and service tokens outside source control;
* do not expose internal service addresses in public documentation unless intentionally published;
* isolate the GPU/model endpoint from untrusted networks;
* treat RAG indexes and conversation logs as potentially sensitive data.

## Verification boundary

Repository metadata confirms the current private Python project and its main branch. Exact module names, provider implementations, endpoints and runtime configuration should be verified against the current source before deployment changes.
