# logstash_poll
Polling JSON Placeholder site with logstash

You need to run the conf file in logstash [REF](https://www.elastic.co/guide/en/logstash/current/configuration.html)  or configure it as a pipeline.

After you run the applicaion fire request to local host port 8080 with json body.

HTTP POST http://localhost:8080

{
    "start":0,
    "chunk":5
}


The above code is a work around for polling in logstash. It will allow you to loop through a site (http://jsonplaceholder.typicode.com/photos?_start=%{start}&_limit=%{chunk}) for any new updates. The pipeline calls self to update the new chunk and start position recived.
