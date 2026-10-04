# SovaV2 project instructions

Read README.md and docs/MILESTONES.md first. They are the current scope and planning index. V1 documents are historical design inputs; assess reuse and licensing before importing code. Current user instructions take precedence.

The current task is initialization and a milestone list. Do not begin detailed implementation or deployment from this task. The complete component plan is reviewed before rebuild execution.

Preserve single-user operation in one ordinary headless Linux user instance. Keep models and runtimes administrator-configurable through validated capability contracts. Do not hard-code a particular deployment host, accelerator or model into the product.

Never commit personal information, passwords, tokens, private keys, access inventories, host addresses, private histories, operational logs or deployment-specific profiles. Keep them in protected state outside the checkout. Use generic placeholders in examples. Verify author and committer use the project's configured GitHub noreply identity before committing. Review staged files and their content before every push; ignore rules and automated secret scanning are additional protections, not substitutes for review.

Workers use fresh briefs, isolated task checkouts and explicit file/resource ownership. Return changes and original checks for orchestrator review. The orchestrator owns interfaces, integration and publication. Repository credentials alone do not enforce this role boundary; inspect branch policy and report gaps rather than assuming worker tokens are branch-limited.

Keep tests proportional to behavior. Direct component checks precede integration; real model and user workflows substantiate runtime claims. Preserve failed or unknown evidence and do not report unexecuted checks as passed. Keep operational receipts private and public documentation concise.
