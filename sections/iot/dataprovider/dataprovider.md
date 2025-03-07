---
author: Benedikte Kallåk
description: This section a toc for data-provider topics
---

# Data provider
A data-provider ingests sensor-data or events to Veracity using different protocols and data-formats. 
- [Sensor data is streamed to Veracity IoT Hub](sensordataingest.md)
- [Sensor data can be uploaded using CSV-files](sensordataingest.md)
- [Events are sent to Veracity using rest-api or streamed using IoT Hub](eventingest.md)

## Protocols
- HTTPS
- AMQP, AMQP over WebSockets
- MQTT, MQTT over WebSockets

## Authentication
Using IoT Hub, data provider needs a private connection string and when using rest-api, [B2C authentication](../dataconsumer/authenticate.md) is required.

## Security Model

-   Users or applications are associated with tenants. Tenants can only ingest or query on data from itself
-   Ingest is restricted to an asset from a predefined list of assets
-   Users or applications must have the appropriate read/write access to ingest on a given asset

## Data format for sensor stream
High frequency data is streamed into Veracity IOT hub from edge solution or from another data platform.  The data format supported are ISO 19848, Veracity-message,  Arundo, Wits, Trisense and CSV. [For more details](sensordataingest.md)

## Data format for events
The payload of the event can be any data structure in JSON format. Each data-structure is defined as a event-type (template). Each event require some meta-data such as asset, topic and timestamp and event-type. [More more information](eventingest.md)
