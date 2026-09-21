# Project Maintenance Guidelines

- **Architecture**: This project is a gateway that aggregates four AI protocols — OpenAI Responses, OpenAI Chat Completions, Anthropic Claude, and Google Gemini — and outputs Antigravity-style Gemini protocol format.
- **Pipeline First**: Keep the pipeline strictly protocol-agnostic. The four protocols are Gemini adapters. Adapters should focus on parameter normalization, payload transformation, and difference adaptation. Downstream pipeline stages should uniformly clean, normalize, and backfill protocol features: thinking blocks, thinking effort, body text, tool schemas, etc.
- **Fix Strategy**: You should always attempt protocol-agnostic fixes in pipeline stages first. You should treat adapter modifications as a last resort.
- **Code Quality**: You should avoid hardcoding, dead code, and unsupported changes. You should prefer root-cause fixes. You should make changes robust and future-proof. You should prefer generalized patterns and wildcards that solve a class of problems over one-off patches.
- **Git & Release**:
  - PR merge commits should include contributor attribution.
  - Release notes should thank contributors and credit the specific ideas/fixes they contributed.

Maintained by @jeikl