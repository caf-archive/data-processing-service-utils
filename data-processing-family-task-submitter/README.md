## Data-Processing-Family-Task-Submitter

The "Data-Processing-Family-Task-Submitter" will use a provided family reference for a family file that has already been indexed to elastic search and use this to query Elastic Search, reconstruct the document and its possible attachments and use this document to construct a policy message and send it to a policy worker queue specified.


Below are the configuration options for the submitter, these are broken into required and optional, optional configurations will have a pre-set default value that will also be listed below.

#### Required:
**FAMILY_REFERENCE:**

The FAMILY_REFERENCE of the document you wish to use from Elastic Search.
i.e. `/inputFolder/myTestTextDocument.docx`

**OUTPUT_QUEUE_NAME:**

The Workflow Worker queue that the output messages should be sent to.
i.e. `document-input`

#### Optional:
**PROJECT_ID:**

The project id to use in the new Document Worker task

- **DEFAULT:** If this is not set it will be set to `1`

**OUTPUT_PARTIAL_REFERENCE:**

The outputPartialReference to use in the new Document Worker task.

- **DEFAULT:** If this is not set it will be set to an empty value.

**TENANT_ID:**

The tenant (customer) id to use in the new Document Worker task.

- **DEFAULT:** If this is not set it will be set to `1`

**WORKFLOW_ID:**

The Workflow Id to use in the new Policy Worker task message.

- **DEFAULT:** If this is not set it will be set to `1`

**CAF_RABBITMQ_HOST:**

The RabbitMq host to use when creating a connection to RabbitMq.

- **DEFAULT:** If this is not set it will be set to `localhost`

**CAF_RABBITMQ_PORT:**

The port that should be use for the application to use to communicate with RabbitMq.

- **DEFAULT:** If this is not set it will be set to `9549`

**CAF_RABBITMQ_USERNAME:**

The username to use when making a connection with RabbitMq.

- **DEFAULT:** If this is not set it will be set to `guest`

**CAF_RABBITMQ_PASSWORD:**
The password to use when making a connection to RabbitMq.

**DEFAULT:** If this is not set it will be set to `guest`





