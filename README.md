# json-pattern-to-xsl-report
A simple pattern to generate xsl report

### Motivation
This pattern will be created to use in multiple languages and projects (personal) 
to validate performance in multiple languages. 

The project will be in PHP.

### Proposal of json for report (0.1)
```json
{
  "name": "example.xlsx",
  "config": {},
  "sheets": [
    {
      "name": "sheet 1",
      "config": {
        "fields": [
          {
            "name": "First field",
            "position": "1",
            "type": "string",
            "json_row_key": "a"
          },
          {
            "name": "Second field",
            "position": "2",
            "type": "string",
            "json_row_key": "b"
          },
          {
            "name": "Third field",
            "position": "3",
            "type": "string",
            "json_row_key": "c"
          },
          {
            "name": "Fourth field",
            "position": "4",
            "type": "string",
            "json_row_key": "d"
          }
        ],
        "first_column": "A",
        "header_line_position": 1,
        "spreedsheet_position": 1
      },
      "data": [
        {
          "a": "l_1_f_1", 
          "b": "l_1_f_2", 
          "c": "l_1_f_3", 
          "d": "l_1_f_4"
        },
        {
          "a": "l_2_f_1", 
          "b": "l_2_f_2", 
          "c": "l_2_f_3", 
          "d": "l_2_f_4"
        },
        {
          "c": "l_3_f_3", 
          "a": "l_3_f_1", 
          "b": "l_3_f_2", 
          "d": "l_3_f_4"
        },
        {
          "a": "l_4_f_1", 
          "b": "l_4_f_2", 
          "c": "l_4_f_3", 
          "d": "l_4_f_4"
        },
        {
          "a": "l_5_f_1", 
          "b": "l_5_f_2", 
          "c": "l_5_f_3", 
          "d": "l_5_f_4"
        },
        {
          "a": "l_6_f_1", 
          "b": "l_6_f_2", 
          "c": "l_6_f_3", 
          "d": "l_6_f_4"
        },
        {
          "a": "l_7_f_1", 
          "b": "l_7_f_2", 
          "c": "l_7_f_3", 
          "d": "l_7_f_4"
        },
        {
          "a": "l_8_f_1", 
          "b": "l_8_f_2", 
          "c": "l_8_f_3", 
          "d": "l_8_f_4"
        }
      ]
    },
    {
      "name": "sheet 2",
      "config": {
        "fields": [
          {
            "name": "First part",
            "position": "1",
            "type": "string",
            "json_row_key": "1"
          },
          {
            "name": "Second part",
            "position": "2",
            "type": "string",
            "json_row_key": "2"
          },
          {
            "name": "Third part",
            "position": "3",
            "type": "string",
            "json_row_key": "3"
          }
        ],
        "first_column": "D",
        "header_line_position": 1,
        "spreedsheet_position": 2
      },
      "data": [
        {
          "1": "This will", 
          "2": "start in", 
          "3": "column D"
        }
      ]
    }
  ]
}
```

### Some considerations

- The property config in first level of json was reserved for future implementations;
- An object sheet will always have three properties. (name, config, data)
