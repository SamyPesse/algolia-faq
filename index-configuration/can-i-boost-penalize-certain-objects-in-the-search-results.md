Definitely!

An easy way to do that is to have an attribute that you will use to separate the featured products from the others.

<pre>[
  {
    "name": "Banana",
    "featured": true
  },
  {
    "name": "Apple",
    "featured": false
  }
]<br></pre>

Add this attribute (e.g. feature = true/false) in your records, and use it **at the top** of the setting _Custom Ranking_.

![](https://s3.amazonaws.com/helpscout.net/docs/assets/557c2386e4b01a224b42b2b3/images/55df015de4b01d7a6a9bdbe6/file-r2eWJTwj90.png)

That’s it! The objects that are tagged “featured” will now have a bonus in the rankings.You can also use the same method with more than 2 levels of featuring. For example, instead of having a boolean value for your attribute _featured_, you could use an integer with values ranging from 0 to 10, which would define 10 different levels of promotion.We’ve decided to use this approach based on attributes, instead of using a more common coefficient based approach, because it offers a better consistency/control, and in the end a better relevance.