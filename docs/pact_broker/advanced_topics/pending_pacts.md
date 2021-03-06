---
title: Pending pacts
---

This page will contain some information about how "pending" pacts work. This is feature is in beta testing but should be released soon. It aims to prevent changed pacts breaking provider builds, while ensuring that provider tests still correctly fail when they break backwards compatiblity.

You can read about the feature here. [http://blog.pact.io/2020/02/24/how-we-have-fixed-the-biggest-problem-with-the-pact-workflow/](http://blog.pact.io/2020/02/24/how-we-have-fixed-the-biggest-problem-with-the-pact-workflow/)

Note that the pending feature is only applicable to the [provider changed workflow](/pact_nirvana/step_4#d-configure-pact-to-be-verified-when-provider-changes), where the list of pacts to be verified are fetched from the Pact Broker. It does not apply to the [contract changed](/pact_nirvana/step_4#e-configure-pact-to-be-verified-when-contract-changes) workflow where the pact URL is passed to the job via the webhook. This is because the pending status of the pact content is calculated based on the tags that the provider will use to publish the verification results, and the 'contract content changed' webhook cannot know this information.
