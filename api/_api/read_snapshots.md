---
title: Read Network Snapshots
position: 230
type: get
description: PATH /network/snapshots?limit=10&offset=2006-01-02T15:04:05.999999999Z07:00&asset=965e5c6e-434c-3fa9-b780-c50f43cd955c
parameters:
  - name: limit
    content: |
      Integer: Max 500
  - name: offset
    content: |
      String: RFC3339Nano
  - name: asset
    content: |
      UUID: OPTION, return all network snapshots or specific asset snapshots.
content_markdown: |-
  Read Mixin network snapshots.

left_code_blocks:
  - code_block: |-
      curl -i --header "Authorization: Bearer eyJhbGciOiJSUzUxMiIsInR5cCI6IkpXVCJ9.eyJleHAiOjE1Mjc1ODYyODQsImlhdCI6MTUyNzU4NjIyNCwianRpIjoiMjZlMjQyM2QtZGUzMC00MTA0LTkyZTQtOTk2MzczOWRkZGE5Iiwic2lkIjoiYWM2ZDFmODYtYTY0Yi00NWRkLTllZmEtN2JmMGVjZjI2MDU2Iiwic2lnIjoiMGIxNGJlZTU5YjE1ODU0MjI1ZTc5ZTU4ZDQwMjZkNDJhYWUyY2Q4ODM4OWE1N2RhNjU4YTRlMjVhNzJlNjRlZSIsInVpZCI6IjMxYjFhMTdjLWFiMzgtNGFhNC05YmM5LWY0NjQyNzEyODExMyJ9.0OUDLd0E1SKslsBJ5nHDE3bC9XKQc_6PPSqBD6Z2E9XYMjQyGht3QWF-uQLohCwbtR_Q7w3_my5MoWM4UyHtWlYh8-mJwg54VFWlhLuFLcWTeG8P971WGVc8oOqNspsEnxDxdBezQVqF1N-XjUtJsVsyJkT6ZEX7VazRm2I2xMM" --header "Content-Type: application/json" --header "Content-length: 0" "https://api.mixin.one/network/snapshots?limit=10&offset=2018-05-29T16:30:24.845515732+08:00"
    title: Curl
    language: bash

right_code_blocks:
  - code_block: |-
      {
        "data":[  
        {  
          "amount":"-1688168",
            "asset":{
              "asset_id":"965e5c6e-434c-3fa9-b780-c50f43cd955c",
              "chain_id":"43d61dcd-e413-450d-80b8-101d5e903357",
              "icon_url":"https://images.mixin.one/0sQY63dDMkWTURkJVjowWY6Le4ICjAFuu3ANVyZA4uI3UdkbuOT5fjJUT82ArNYmZvVcxDXyNjxoOv0TAYbQTNKS=s128",
              "name":"Chui Niu Bi",
              "symbol":"CNB",
              "type":"asset"
            },
            "created_at":"2018-05-29T09:31:04.202186212Z",
            "data":"",
            "snapshot_id":"529934b0-abfd-43ab-9431-1805773000a4",
            "source":"TRANSFER_INITIALIZED",
            "type":"snapshot"
        },
        ...
        ]
      }
    title: Response
    language: json
---
