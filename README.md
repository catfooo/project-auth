# ive created createdAt field, and added process to handle logout the user.
my local storage current has no access token, which indicates ive successfully logged out.
but the problem is with creating new user.
i highyly doubt that i was able to do this.
because this likely supposed to create multiple user probably?
i remember i tested this thousand times yesterday.
and what i have currently is, only

{"_id":{"$oid":"6585928bba80c151c3f2452f"},"name":"1","email":"2","password":"$2a$10$tV310roYSSsAlMmOmRjn9u0dTq2m1wJ4/.aSy0iNIao0Lx/D.Gqu2","accessToken":"9d618fd67e409361a70c34c80d7cf0e72487c430b05d12bf92d48dd53e0e1a58457399671f4f08011f0aca161c1a212e33a0295bcf108bb41b73707faf6248c65338d357ba8c737956950c27f901e8a0f2d18ec7200a63dc7a4d857180b6870f5be49cc2d4407b78299df5263ce5a332fd964cfe9fd9652cb435bbee778029c5","__v":{"$numberInt":"0"}}

this single document.
not multiple document with several 1 2 3 that i input through input field.
so, in summary, although i have something like this at browser console every single time that i submit data 1 2 3 with creating new user,

{id: '6586cd1f40383a4d4046ca18', accessToken: 'a77e03cc5eb178cbd396a6bcc2045b9171f5fc5c6cb2228a2f…cccc2395ac235887c4b469fc204ccfe8f8883cdf26f9af1c2'}

this indicates this is not happeneing database side. probably only for server side,
or im not even sure with this, bcs accesstoken is what i implemented at backend.
it works only for backend code, server.js.


# so, what is the actual problem currently?
when i create user with 4 5 6 with input field, it doesnt update database cloud.
what i see is only formal 1 2 3. of course, not with createdAt field.
why i could create 1 2 3 before,
and why i cant create 4 5 6 currently?

# err msg from dev console
it is... very familiar, cors error.
this happened before to me, 
when i submit wrong user field.
but i highly doubt this process, bcs i was able to create user with 1 2 3 before, probably.
forst, ill force this cors error to removed, just like what i did before, with unable cors,
and ill see how i handle this after.

{id: '6586cd1f40383a4d4046ca18', accessToken: 'a77e03cc5eb178cbd396a6bcc2045b9171f5fc5c6cb2228a2f…cccc2395ac235887c4b469fc204ccfe8f8883cdf26f9af1c2'}accessToken: "a77e03cc5eb178cbd396a6bcc2045b9171f5fc5c6cb2228a2f0015d7e557dc273878d007f60608cf81e9d82e61f46e60edcdd5cae17f5b5bf5c2c834228962bdbc56e0777b48a23e996bfe5ee32712bf9b330376b6608af8d98ee34fc8eadc8240eb886d92d9624cccc2395ac235887c4b469fc204ccfe8f8883cdf26f9af1c2"id: "6586cd1f40383a4d4046ca18"[[Prototype]]: Object
localhost/:1 Access to fetch at 'https://one8-y5ov.onrender.com/users' from origin 'http://localhost:5173' has been blocked by CORS policy: Response to preflight request doesn't pass access control check: No 'Access-Control-Allow-Origin' header is present on the requested resource. If an opaque response serves your needs, set the request's mode to 'no-cors' to fetch the resource with CORS disabled.
App.jsx:19 
        
        
       POST https://one8-y5ov.onrender.com/users net::ERR_FAILED
postID @ App.jsx:19
handleButtonClick @ App.jsx:68
callCallback2 @ react-dom_client.js?v=ba23b5ff:3672
invokeGuardedCallbackDev @ react-dom_client.js?v=ba23b5ff:3697
invokeGuardedCallback @ react-dom_client.js?v=ba23b5ff:3731
invokeGuardedCallbackAndCatchFirstError @ react-dom_client.js?v=ba23b5ff:3734
executeDispatch @ react-dom_client.js?v=ba23b5ff:7014
processDispatchQueueItemsInOrder @ react-dom_client.js?v=ba23b5ff:7034
processDispatchQueue @ react-dom_client.js?v=ba23b5ff:7043
dispatchEventsForPlugins @ react-dom_client.js?v=ba23b5ff:7051
(anonym) @ react-dom_client.js?v=ba23b5ff:7175
batchedUpdates$1 @ react-dom_client.js?v=ba23b5ff:18907
batchedUpdates @ react-dom_client.js?v=ba23b5ff:3577
dispatchEventForPluginEventSystem @ react-dom_client.js?v=ba23b5ff:7174
dispatchEventWithEnableCapturePhaseSelectiveHydrationWithoutDiscreteEventReplay @ react-dom_client.js?v=ba23b5ff:5476
dispatchEvent @ react-dom_client.js?v=ba23b5ff:5470
dispatchDiscreteEvent @ react-dom_client.js?v=ba23b5ff:5447
Visa 15 ramar till
Visa färre
VM15:1 error: TypeError: Failed to fetch
    at postID (App.jsx:19:30)
    at handleButtonClick (App.jsx:68:5)
    at HTMLUnknownElement.callCallback2 (react-dom_client.js?v=ba23b5ff:3672:22)
    at Object.invokeGuardedCallbackDev (react-dom_client.js?v=ba23b5ff:3697:24)
    at invokeGuardedCallback (react-dom_client.js?v=ba23b5ff:3731:39)
    at invokeGuardedCallbackAndCatchFirstError (react-dom_client.js?v=ba23b5ff:3734:33)
    at executeDispatch (react-dom_client.js?v=ba23b5ff:7014:11)
    at processDispatchQueueItemsInOrder (react-dom_client.js?v=ba23b5ff:7034:15)
    at processDispatchQueue (react-dom_client.js?v=ba23b5ff:7043:13)
    at dispatchEventsForPlugins (react-dom_client.js?v=ba23b5ff:7051:11)
eval @ VM15:1
overrideMethod @ console.js:213
postID @ App.jsx:44
await in postID (asynkron)
handleButtonClick @ App.jsx:68
callCallback2 @ react-dom_client.js?v=ba23b5ff:3672
invokeGuardedCallbackDev @ react-dom_client.js?v=ba23b5ff:3697
invokeGuardedCallback @ react-dom_client.js?v=ba23b5ff:3731
invokeGuardedCallbackAndCatchFirstError @ react-dom_client.js?v=ba23b5ff:3734
executeDispatch @ react-dom_client.js?v=ba23b5ff:7014
processDispatchQueueItemsInOrder @ react-dom_client.js?v=ba23b5ff:7034
processDispatchQueue @ react-dom_client.js?v=ba23b5ff:7043
dispatchEventsForPlugins @ react-dom_client.js?v=ba23b5ff:7051
(anonym) @ react-dom_client.js?v=ba23b5ff:7175
batchedUpdates$1 @ react-dom_client.js?v=ba23b5ff:18907
batchedUpdates @ react-dom_client.js?v=ba23b5ff:3577
dispatchEventForPluginEventSystem @ react-dom_client.js?v=ba23b5ff:7174
dispatchEventWithEnableCapturePhaseSelectiveHydrationWithoutDiscreteEventReplay @ react-dom_client.js?v=ba23b5ff:5476
dispatchEvent @ react-dom_client.js?v=ba23b5ff:5470
dispatchDiscreteEvent @ react-dom_client.js?v=ba23b5ff:5447
Visa 16 ramar till
Visa färre


# oh no. i think ive fucked this up.
so when i enabled no cors mode, the dev console started to spit out nothing.
not even single

{"_id":{"$oid":"6585928bba80c151c3f2452f"},"name":"1","email":"2","password":"$2a$10$tV310roYSSsAlMmOmRjn9u0dTq2m1wJ4/.aSy0iNIao0Lx/D.Gqu2","accessToken":"9d618fd67e409361a70c34c80d7cf0e72487c430b05d12bf92d48dd53e0e1a58457399671f4f08011f0aca161c1a212e33a0295bcf108bb41b73707faf6248c65338d357ba8c737956950c27f901e8a0f2d18ec7200a63dc7a4d857180b6870f5be49cc2d4407b78299df5263ce5a332fd964cfe9fd9652cb435bbee778029c5","__v":{"$numberInt":"0"}}

that i used to had when i submit with 1 2 3 at least. wait, was i getting this with 4,5,6? cant remember so ill go up and see.
it is probably saying i had this first when i tested with 4 5 6 ?
and then, maybe i enabled no cors mode and it just stopped to work?
so i disabled this again, and totally fucked up. stopped to working, giving me nothing.
i highly regret that i backup this before i try enable no cors mode
but like
how would i know it?
do i need to back up every single time that i try implement new change every single time?
with creating every single new repo every single time?
if so, im out. it doesnt makes sense.
i mean, the others should being working better than what i am.
i dont think others have possiblity with this much fucked up as i have.
but how can i know how others are doing?
conversation system is totally blocked wity my school currently. not helping me at all.
but what i need is community, i need this so bad, to exchange each others status and exchange how each others work
when the face this kind of ridiculous working situation
i hope rly, technigo had gave me this kind of working invironment
i was expecting exactly this when i applied to this school
there is no point to just learn self when im paying and participating at school
so this is wrong. what i can say is this is wrong. i wish my wish has voice and goes to someone who understands me



# while i was mad...

and then, the dev console finally gave me the result.
so, it was not fucked up at all, but it was just fucking slow to respond.
just usual cors error when i send 4 5 6 with disabled no cors mode.
so need to enable this and see what happens again xD

(the usual cors error that i used to have when having problem with input field)
Access to fetch at 'https://one8-y5ov.onrender.com/users' from origin 'http://localhost:5173' has been blocked by CORS policy: No 'Access-Control-Allow-Origin' header is present on the requested resource. If an opaque response serves your needs, set the request's mode to 'no-cors' to fetch the resource with CORS disabled.
App.jsx:19 
        
        
       POST https://one8-y5ov.onrender.com/users net::ERR_FAILED
postID @ App.jsx:19
handleButtonClick @ App.jsx:68
callCallback2 @ react-dom_client.js?v=ba23b5ff:3672
invokeGuardedCallbackDev @ react-dom_client.js?v=ba23b5ff:3697
invokeGuardedCallback @ react-dom_client.js?v=ba23b5ff:3731
invokeGuardedCallbackAndCatchFirstError @ react-dom_client.js?v=ba23b5ff:3734
executeDispatch @ react-dom_client.js?v=ba23b5ff:7014
processDispatchQueueItemsInOrder @ react-dom_client.js?v=ba23b5ff:7034
processDispatchQueue @ react-dom_client.js?v=ba23b5ff:7043
dispatchEventsForPlugins @ react-dom_client.js?v=ba23b5ff:7051
(anonym) @ react-dom_client.js?v=ba23b5ff:7175
batchedUpdates$1 @ react-dom_client.js?v=ba23b5ff:18907
batchedUpdates @ react-dom_client.js?v=ba23b5ff:3577
dispatchEventForPluginEventSystem @ react-dom_client.js?v=ba23b5ff:7174
dispatchEventWithEnableCapturePhaseSelectiveHydrationWithoutDiscreteEventReplay @ react-dom_client.js?v=ba23b5ff:5476
dispatchEvent @ react-dom_client.js?v=ba23b5ff:5470
dispatchDiscreteEvent @ react-dom_client.js?v=ba23b5ff:5447
Visa 15 ramar till
Visa färre
VM15:1 error: TypeError: Failed to fetch
    at postID (App.jsx:19:30)
    at handleButtonClick (App.jsx:68:5)
    at HTMLUnknownElement.callCallback2 (react-dom_client.js?v=ba23b5ff:3672:22)
    at Object.invokeGuardedCallbackDev (react-dom_client.js?v=ba23b5ff:3697:24)
    at invokeGuardedCallback (react-dom_client.js?v=ba23b5ff:3731:39)
    at invokeGuardedCallbackAndCatchFirstError (react-dom_client.js?v=ba23b5ff:3734:33)
    at executeDispatch (react-dom_client.js?v=ba23b5ff:7014:11)
    at processDispatchQueueItemsInOrder (react-dom_client.js?v=ba23b5ff:7034:15)
    at processDispatchQueue (react-dom_client.js?v=ba23b5ff:7043:13)
    at dispatchEventsForPlugins (react-dom_client.js?v=ba23b5ff:7051:11)

    (but wait, where is familiar id and accesstoken that i used to got when submit?
    in this case, it doesnt contains log with id and accesstoken that looks like this
    
{id: '6586cd1f40383a4d4046ca18', accessToken: 'a77e03cc5eb178cbd396a6bcc2045b9171f5fc5c6cb2228a2f…cccc2395ac235887c4b469fc204ccfe8f8883cdf26f9af1c2'}

which means this is the current problem.)

so, currently, when i submit 4 5 6 at input field, i am having both cors err and 'not generated console log for id and accesstoken err' if i call this correctly.

and, before, like yesterday, when i submit 1 2 3 , i had no cors error, neither 'not generated ... err'. i had console log actually yesterday.

oh no. i rly dont know how to proceed.
lets shut up and just handle cors feature first. at least, i have possiblity of get rid of cors error at least. 



# i enabled this, mode: 'no-cors',
and getting this. rly clear.

VM15:1 error: SyntaxError: Unexpected end of input (at App.jsx:31:42)
    at postID (App.jsx:31:42)


-> i think im having this bcs i enabled 'no-cors', which blocks to make valid JSON.
so.. not related to no-cors probably?
but, like before, yesterday, when i handle 1 2 3 submit, i had same problem with cors,
and i solved this with 1.having valid input first 2. and then disable no-cors
this is related with cors error. what was yesterday?
#1. without having no cors mode, i had cors error.
#2. with having enabled no cors mode, i had probably input err, probably. i cant remember but likely like this. 
#3. by fixing input problem, and disabling no cors mode, i could access to welcome page? or i could manage create user? or i could store the accesstoken? cant remember rly, but something between this, meaning i felt ive solved the problem at that time yesterday.

# so... what to do now?
make sure my current input is valid.
-> haha, chatgpt says 4,5,6 is no problem. then what?
would 1,2,3 had problem also?
then how would i post at the cloud database? no clue at all xDDDDD
if i cant fix input bcs i cant find any problem there, then no meaning of taking care of cors now. bcs it seemed work yesterday, but not for today. cant take same approach,
or i might mistaken something. probably i failed yesterday and thoought i was succeed with input and cloud and things like that xDDDD rly not sure how to start or what to continue

lets disable no cors first then
and then forget everything that happened today,
and then try to take a look again with current err msg that i got from dev console from browser,
which saying

VM15:1 error: SyntaxError: Unexpected end of input (at App.jsx:31:42)
    at postID (App.jsx:31:42)




# was able to inject accesstoken direct to local storage and see the result saying welcome user.
what next?
so token is working
but creating user is not working
but was working yesterday, or seemed to at least
so... like why? rly frustrated


# i cant register user and dont know why

# i register 1 2 3 just like ive did yesterday, and chrome dev console is not responding. might server is too slow or having problem somewhere. rly feel bad about this slow process. but no. while i try this and that while waiting, it spitted out this familiar console log at chorme dev console.

saying,
{id: '6586e0515cd947fdd72e65a9', accessToken: 'c46daf26ac72a15ac28378af23f4bfbcb11c3325eaa1f6be94…6a1aacb8408632505d779badbf24499859651c33b194bc5b1'}

showing, 
welcome, user


where this accesstoken comes from?
super sure not comes from, or stored at cloud mongodb.
bcs when i refresh, what i see is only this,

_id
6585928bba80c151c3f2452f
name
"1"
email
"2"
password
"$2a$10$tV310roYSSsAlMmOmRjn9u0dTq2m1wJ4/.aSy0iNIao0Lx/D.Gqu2"
accessToken
"9d618fd67e409361a70c34c80d7cf0e72487c430b05d12bf92d48dd53e0e1a58457399…"
__v
0


which is very much different from what i got.


it seems pretty sure it generetes token and stuff when i submit at register.
but it seems it is not storing the data at cloud mongodb.
but bcs it stores 'this' data, not loads the data from 'cloud mongo', at localstorage,
the browser uses this token to log in,
so pretty much not about the mongodb cloud itself.
haha having been doing wrong structure. this is not communicating with cloud server but with my very local.


so the correct following step should be,
when i register,
it stores the user data at cloud first.
idk why 123 before seemed to be happen to be stored for cloud.

but it is clear that the data im seeing from cloud
{"_id":{"$oid":"6585928bba80c151c3f2452f"},"name":"1","email":"2","password":"$2a$10$tV310roYSSsAlMmOmRjn9u0dTq2m1wJ4/.aSy0iNIao0Lx/D.Gqu2","accessToken":"9d618fd67e409361a70c34c80d7cf0e72487c430b05d12bf92d48dd53e0e1a58457399671f4f08011f0aca161c1a212e33a0295bcf108bb41b73707faf6248c65338d357ba8c737956950c27f901e8a0f2d18ec7200a63dc7a4d857180b6870f5be49cc2d4407b78299df5263ce5a332fd964cfe9fd9652cb435bbee778029c5","__v":{"$numberInt":"0"}}
this one, happened to be stored accidently, or some process with i dont know,
or by mistake,


and i just want to make sure my app is currently not storing user at cloud. 
i think there is possiblity , regardless of trial of 456, 
when i try 123, there is already 123.
there is no process for validate this already existing data or not
so can be this-related-problem,

but just wanted to make sure i can register first.

it is 14:36
but im rly feeling uncomfortable bcs of problem that related to the place i chose
for todays work
im not sure. will i be able to manage recover myself today within this short moment?

idk. im not sure. but i want to give try,
bcs today is good day, i dont want to lose today
just due to minor problem such like this. 

wish me to manage to come back.
i will register the user somehow, i strongly want this