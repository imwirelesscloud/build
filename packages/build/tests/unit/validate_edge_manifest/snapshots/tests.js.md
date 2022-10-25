# Snapshot report for `tests/unit/validate_edge_manifest/tests.js`

The actual snapshot is saved in `tests.js.snap`.

Generated by [AVA](https://avajs.dev).

## should detect invalid route pattern in manifest

> Snapshot 1

    `[␊
      {␊
        "instancePath": "/routes/2/pattern",␊
        "schemaPath": "#/properties/routes/items/properties/pattern/errorMessage",␊
        "keyword": "errorMessage",␊
        "params": {␊
          "errors": [␊
            {␊
              "instancePath": "/routes/2/pattern",␊
              "schemaPath": "#/properties/routes/items/properties/pattern/format",␊
              "keyword": "format",␊
              "params": {␊
                "format": "regexPattern"␊
              },␊
              "message": "must match format \\"regexPattern\\"",␊
              "emUsed": true␊
            }␊
          ]␊
        },␊
        "message": "must match format /^\\\\^.*\\\\$$/"␊
      }␊
    ]`

## should detect missing property in manifest

> Snapshot 1

    `[␊
      {␊
        "instancePath": "",␊
        "schemaPath": "#/errorMessage",␊
        "keyword": "errorMessage",␊
        "params": {␊
          "errors": [␊
            {␊
              "instancePath": "/bundles/0",␊
              "schemaPath": "#/properties/bundles/items/required",␊
              "keyword": "required",␊
              "params": {␊
                "missingProperty": "format"␊
              },␊
              "message": "must have required property 'format'",␊
              "emUsed": true␊
            }␊
          ]␊
        },␊
        "message": "Couldn't validate Edge Functions manifest.json"␊
      }␊
    ]`

## should detect extra property in manifest

> Snapshot 1

    `[␊
      {␊
        "instancePath": "",␊
        "schemaPath": "#/errorMessage",␊
        "keyword": "errorMessage",␊
        "params": {␊
          "errors": [␊
            {␊
              "instancePath": "/routes/0",␊
              "schemaPath": "#/properties/routes/items/additionalProperties",␊
              "keyword": "additionalProperties",␊
              "params": {␊
                "additionalProperty": "extra"␊
              },␊
              "message": "must NOT have additional properties",␊
              "emUsed": true␊
            }␊
          ]␊
        },␊
        "message": "Couldn't validate Edge Functions manifest.json"␊
      }␊
    ]`