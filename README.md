## Overview
ERC20 ranking restful api

## Endpoint
Default endpoints:

| API | URL | Protocol |
|-------|:------------:|:------------:|
| RESTful |http://39.107.32.62:8014 | HTTP |

## RPC methods
* [GetErc20Ranking](#geterc20ranking)

## RPC API Reference

#### GetErc20Ranking
Return the state of the neb.

| Protocol | Method | API |
|----------|--------|-----|
| HTTP | GET |  /ranking |


###### Parameters
none

###### Returns
`date`: Date range.

`address`: Erc20 smart contract name and address string.

`median`: Median address stake.

`weight`: In-and-Out amount.

`score`: Ranking score.

`in_degree`: Transaction graph in degree.

`in_val`: Transaction received value.

`in_outs`: The number of active address.

###### HTTP Example
```
// Request
curl -i -H 'Content-Type: application/json' -X GET http://39.107.32.62:8014/ranking

// Result
{
   "result":[
      {
         "date":"20191206-20191209",
         "address":"USDT_0xdac17f958d2ee523a2206206994597c13d831ec7",
         "median":29141.888083307782,
         "weight":47396.01068012931,
         "score":4406.871726037682,
         "in_degree":121507,
         "out_degree":121507,
         "degrees":243014,
         "in_val":28665.361683180956,
         "out_val":28665.361683180272,
         "in_outs":71903
      },
      ...
   ],
   "has_more":false,
   "id":null
}
```
