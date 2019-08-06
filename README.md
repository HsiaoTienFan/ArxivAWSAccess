# Accessing bulk Arxiv data
I am very new to AWS and I absolutely hate using command line tools. That being said, it is what it is, and to develop anything useful we need to use all tools available. 

Recently I wanted to copy the arxiv data to my own S3 bucket, and couldn't find a tutorial that just outright taught me how to move the data from their S3 bucket to mine.

I eventually figured it out, but just as documentation, this repo will serve as a reminder of how and what was done. If it ends up helping anyone along the way its a bonus

## Learnings

Off the bat I just want to list what I used:

```
aws s3 cp --recursive s3://arxiv/pdf/ s3://MY_OWN_BUCKET --request-payer requester
```

This copied everything in the arxiv S3 bucket to my own.
 
 ***NOTE!!!!!!! The requester pays for the data transfer*** 

I will continue to add stuff as I go