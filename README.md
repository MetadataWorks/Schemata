# Schemata
Metadata schemata for more Findable, Accessible, Interoperable and Reusable (FAIR) data

# Style

# Properties:
Naming:camelCase + try to avoid numbers. If they are needed add them as a suffix i.e. chars80 rather than 80chars.
Attributes: 
- "$id": camelCase,include path to the property "#/properties/path/name, example: "#/properties/version" or "#/summary/publisher"
- "title": Capital Case, example: "Dataset Version"
- "description": always include a descriptions of the property
- "$ref": if the property uses a definition/format that is generalisable, create a new definition and refer to it, otherwise use "format"  & "type" attributes
- "allOf": if the property has more than once definition include this
- "$comment": if applicable insert a comment
- "examples": always include an example value(s), example: ["1.1.0"] 
- "default": include a default value if applicable

# Definitions:
Include all the definitions at the bottom of the schema. All definitions should be sorted alphabetically.
Naming: camelcase
Attributes:
- "$id": camelCase,include path to the definitions "#/definitions/path/name, example: "#/definitions/observation"
- "type": if the type is complex i.e. "object" include:
  - "required": example: ["observedNode"]
  - "additionalProperties: true/false if applicable]
  - "properties"
- "type": if the type is simple include the type information i.e. minLength, maxLength, enum, pattern
