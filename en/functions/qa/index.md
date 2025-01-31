---
title: "{{ sf-full-name }}. Questions and answers"
description: "How do I get the logs of my activity in {{ sf-full-name }}? Find the answer to this and other questions in this article."
---

# General questions about {{ sf-name }}

{% include [logs](../../_qa/logs.md) %}

#### How do I download a ZIP archive with the source code to update the Serverless function via the CLI? {#version-create}

To create a [function](../concepts/function.md) version from a ZIP file, execute:

```bash
yc serverless function version create --source-path
```

You can learn more about downloading the code in the guide on [{#T}](../../functions/operations/function/version-manage.md).

#### Size of source code archive for uploading to {{ sf-name }} {#file-size}

You can upload a file up to 3.5 MB in size directly. A larger file must be [uploaded via {{ objstorage-full-name }}](../../storage/operations/objects/upload.md). You can learn more in the [documentation](../../functions/operations/function/version-manage.md).

#### I am not the owner of the cloud, but I have been granted access. What rights/roles do I need to be able to publish a feature? {#roles}

For function access, you need the `admin` or `resource-manager.clouds.owner` role. For more see the [documentation](../security/index.md).

#### As from Node.js code in {{ sf-name }} to access an environment variable? {#env}

To access environment variables, use the `process.env` global variable. For more see the [documentation](https://nodejs.org/dist/latest-v8.x/docs/api/process.html#process_process_env).

#### Which Python modules can be used when working with {{ sf-name }}? How to connect new modules? {#python}

You can upload modules as a ZIP file up to 3.5 MB in size. A larger file must be [uploaded via {{ objstorage-name }}](../../storage/operations/objects/upload.md). For more see the [documentation](../quickstart/create-function/python-function-quickstart.md).

#### Invoking cloud functions for Alice's skills is free. If I invoke another one of my cloud functions from a skill cloud function? Will that be free as well? {#alice-pricing}

Such calls will be charged per the [{#T}](../pricing.md).

#### I want to increase my quotas. How do I determine the appropriate values for them? {#quotas}

For more information on which quotas to increase and to what extent, see [{#T}](../concepts/limits.md#related-quotas).
