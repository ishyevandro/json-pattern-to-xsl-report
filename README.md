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
          "field_1",
          "field_2",
          "field_3",
          "field_4"
        ],
        "first_column": "A",
        "header_line": 1
      },
      "data": [
        ["l_1_f_1", "l_1_f_2", "l_1_f_3", "l_1_f_4"],
        ["l_2_f_1", "l_2_f_2", "l_2_f_3", "l_2_f_4"],
        ["l_3_f_1", "l_3_f_2", "l_3_f_3", "l_3_f_4"],
        ["l_4_f_1", "l_4_f_2", "l_4_f_3", "l_4_f_4"],
        ["l_5_f_1", "l_5_f_2", "l_5_f_3", "l_5_f_4"],
        ["l_6_f_1", "l_6_f_2", "l_6_f_3", "l_6_f_4"],
        ["l_7_f_1", "l_7_f_2", "l_7_f_3", "l_7_f_4"],
        ["l_8_f_1", "l_8_f_2", "l_8_f_3", "l_8_f_4"]
      ]
    },
    {
      "name": "sheet 2",
      "config": {
        "fields": [
          "field_1",
          "field_2",
          "field_3"
        ],
        "first_column": "D",
        "header_line": 1
      },
      "data": [
        ["This will", "start in", ""]
      ]
    }
  ]
}
```

### Some considerations

- The property config in first level of json was reserved for future implementations;
- An object sheet will always have three properties. (name, config, data)
