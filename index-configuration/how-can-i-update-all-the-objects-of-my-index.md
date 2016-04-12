If you want to update all of your objects, you may want to use our  [atomical re-indexing](https://www.algolia.com/doc/ruby#atomical-re-indexing) feature. It allows you to update everything while keeping your existing search running with the current data. For that, you will need to create a temporary index, configure it like your production index, push the whole data to it and then replace your current index by this temporary index.

Beware, when you make the switch from one index to the other, the slaves will automatically get transferred. This means that the settings of your temporary index must not have any slaves.Here's the procedure to do that (in Ruby):

1.  Create a new index `temp_index = Algolia::Index.new "my_temp_index"`
2.  Copy the settings (and remove the slaves if needed) `temp_index.set_settings(prod_index.get_settings.merge({ slaves: [] }))`
3.  Import the data in the `temp_index.add_objects ....`
4.  Replace the index `client.move_index(‘my_temp_index’, ‘my_index’)`