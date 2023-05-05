# assigment

This is API Gateway that will be used for rate limit handling for the service email and sms,
it's made with Spring cloud Gatway, Redis and Postgres, apart from rate limit management it will be used for rate rules management for our clients, 
we separte the rate limit based on the service needed that meas sms and email have the different rate limit applied 
to test this Gateway we  made a bash file to simulate  the rate limit with the below content 

Email
#!/bin/bash
while :
do
curl -s -o /dev/null -I -w  "%{http_code}" -X GET http://localhost:85/email/
echo ""
done



Sms
#!/bin/bash
while :
do
curl -s -o /dev/null -I -w  "%{http_code}" -X GET http://localhost:85/sms/
echo ""
done

