We definitely recommend to search from the front-end! For multiple reasons:

1.  **Speed**. A front-end implementation will hit our servers directly, without going through your backend. It can be up to 10x faster for the end-user to retrieve the results.
2.  **DSN**. We have a distributed API allowing you to select [multiple datacenters around the world](https://www.algolia.com/dsn). This allows your users to target the closest server, which has a huge impact on latency. This can only work with a front-end implementation.
3.  **Availability**. With a back end implementation, you force some network routes. Even if there is only a local problem in the network, all of your users will be affected. Having a front-end implementation means only a subset of your users will be affected if there's a network problem.

If you feel like a back-end implementation would work better in your case, don't hesitate to [get in touch](mailto:support@algolia.com) with us.