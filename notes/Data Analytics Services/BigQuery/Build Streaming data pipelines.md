# Build Streaming data pipelines
Based on [[Cloud Pub Sub]] and [[Example of End-to-end Data Pipeline]].

### Set streaming option to true: 
`options.view_as(StandardOptions).streaming = True`
### Reading from stream
instead of `beam.io.readFromTxt()`, we must use `beam.io.ReadFromPubSub()`

Then remove the pipelines:
- cleaned_data
- delivered_orders
- other_orders
This because streams are unbounded data and can't be grouped

### Adding wait_until_finish()
adding after  `ret=p.run()`:
`ret.wait_until_finish()`

> Note that the code after this line won't run until the finish of the pub/sub.
> If we want to launch other commands we must creat a new thread and launch it before `wait_until_finish()`