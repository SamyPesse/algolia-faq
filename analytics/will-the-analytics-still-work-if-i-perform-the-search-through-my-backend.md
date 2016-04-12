The aggregation of the queries to retrieve the latest query uses the IP or the user token to work efficiently. If the queries are made from your backend server, the IP will be the same for all of the queries. We're supporting the following HTTP header to forward the IP of your end-user to the engine, you just need to set it for each query:

<pre>X-Forwarded-For: IP_OF_THE_END_USER</pre>

It's also possible to use the following (custom) header to track users that have the same IP or to track users that use different devices with:

<pre>X-Algolia-UserToken: UID_OF_THE_END_USER</pre>