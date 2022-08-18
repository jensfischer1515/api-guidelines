---
type: MUST
id: R200001
---

# use CloudEvents format to encode events

Events must be encoded as [CloudEvents 1.0.2](https://github.com/cloudevents/spec/blob/v1.0.2/cloudevents/spec.md).

The CloudEvents specification defines a number of required and optional [context attributes](https://github.com/cloudevents/spec/blob/v1.0.2/cloudevents/spec.md#context-attributes). Context attributes can be treated as metadata about the event, that can be extracted without knowing the structure of the event itself.

The following table shows the most important context attributes and includes event guidelines rules, which are specific to some context attributes.

| Context attribute                                                                                      | Event Guideline rules                                                         |
| ------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------- |
| [id](https://github.com/cloudevents/spec/blob/v1.0.2/cloudevents/spec.md#id)                           |                                                                               |
| [source](https://github.com/cloudevents/spec/blob/v1.0.2/cloudevents/spec.md#source-1)                 | [MUST provide meaningful `source` context attribute](@guidelines/R200010)     |
| [specversion](https://github.com/cloudevents/spec/blob/v1.0.2/cloudevents/spec.md#specversion)         | only '1.0' allowed                                                            |
| [type](https://github.com/cloudevents/spec/blob/v1.0.2/cloudevents/spec.md#type)                       | [MUST follow naming scheme for `type` context attribute](@guidelines/R200009) |
| [datacontenttype](https://github.com/cloudevents/spec/blob/v1.0.2/cloudevents/spec.md#datacontenttype) |                                                                               |
| [dataschema](https://github.com/cloudevents/spec/blob/v1.0.2/cloudevents/spec.md#dataschema)           |                                                                               |
| [time](https://github.com/cloudevents/spec/blob/v1.0.2/cloudevents/spec.md#time)                       | [MUST provide event time in UTC](@guidelines/R200011)                         |
| [subject](https://github.com/cloudevents/spec/blob/v1.0.2/cloudevents/spec.md#subject)                 |                                                                               |