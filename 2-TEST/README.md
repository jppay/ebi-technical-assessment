# Testing the DRS Starter Kit
  
## 1. Testing strategy  
Once DRS Starter Kit is deployed and running, it can be tested for the following test scenarios  
- Send a `GET` Request to `http://localhost:5000/ga4gh/drs/v1/objects/{object_id}` endpoint with the below listed input DRS object IDs and verify that the outputs are as expected

|object_id | Expected Status Code | Expected Content Type |
| -------- | -------------------- | --------------------- |
|8e18bfb64168994489bc9e7fda0acd4f  | 200 | JSON |
|ecbb0b5131051c41f1c302287c13495c  | 200 | JSON |
|xx18bfb64168994489bc9e7fda0acd4f  | 404 | JSON |  
- Verify that the service returns output of `400` when a malformed endpoint is called  

## 2. Testing  
All the above mentioned test cases have been coded is available at `../Tech_Lead_Coding_Interview/venv/tests/drs_id_test.py`  
It can executed as  
```
cd venv/tests
```  
```
drs_id_test.py
```  
## NOTE: 
The `pytest` and `responses` packages required to run the tests is included in the `requirements.txt` and will be installed as part of the deployment. 
