<!-- @format -->

"start"

1. during architecture part 21:00
   why do we need seperate backend for communicating with bank server (cause it needs to be highly available service thus deploying it seperatly is better).
2. why not do it on frontend (user can spoof it right??)
   what if you transacvtion got external issue like i made payment and wifi went down money got debited but cant see on frontend(its highly unreliable ) (so let the bank hit out backend and put in database).

   another scenario what if you immediately close the frontend page (and then make payment) how would our appluication know. (so having a seperate backend is important)

   another sceneraio why not merge it with the same deployment (reason is we can't aniticipate the traffic like i saw in hotstar video ) cause backend for updation is cruicial part of application we cant affort to let it have any down time,
