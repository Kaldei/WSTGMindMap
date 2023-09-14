#graphql 

Mutation Query (will create and then return created or modified value. Can be used to extract data from database.

```bash
curl -s -X POST \ 
-d '{ "query": "mutation { addReview(articleId: 12, review: \"This is a new review\") { valueToExtractId, articleId } }" }' \
http://[TAGET_IP]/  | jq
```
 
