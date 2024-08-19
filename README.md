<!-- @format -->

"start"


Notes:- https://projects.100xdevs.com/tracks/Paytm/paytm17-1

1. during architecture part 21:00
   why do we need separate backend for communicating with bank server (cause it needs to be highly available service thus deploying it separately is better).
2. why not do it on frontend (user can spoof it right??)
   what if you transaction got external issue like i made payment and wifi went down money got debited but cant see on frontend(its highly unreliable ) (so let the bank hit out backend and put in database).

![image](https://github.com/user-attachments/assets/adfed094-2643-453c-ad9b-ab055291eba6)

   another scenario what if you immediately close the frontend page (and then make payment) how would our application know. (so having a separate backend is important)
   another scenario why not merge it with the same deployment (reason is we can't aniticipate the traffic like i saw in hotstar video ) cause the backend for updation is crucial part of the application we can't afford     to let it have any downtime,

3. another service is when we want to send money from wallet to bank (if bank is down we cant send user message to try again later or we can have another service )
   ![image](https://github.com/user-attachments/assets/3707533d-7dda-4d60-ba42-be6f45a1388a)

4. or another better approach is haveing a queue (store all there and try again latter (auto hits the server after some time )) (that queue task must be performed sequentially cause if another services picos same user     then its highly likely we will end up sending multiple request) (thus only sequential order to be followed )
   ![image](https://github.com/user-attachments/assets/25c61413-173f-46a7-b148-0a0179e96892)



content from Cohort 0-1 by 100xdev
