# logstash_poll
Polling JSON Placeholder site with logstash

You need to run the conf file in logstash [REF](https://www.elastic.co/guide/en/logstash/current/configuration.html)  or configure it as a pipeline.

After you run the applicaion fire request to local host port 8080 with json body.

HTTP POST http://localhost:8080

{
    "start":0,
    "chunk":5
}
