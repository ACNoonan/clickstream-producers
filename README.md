# clickstream-producers
Version control for developing Kafka producers that generate mock clickstream data.


clickstream.py
 - Initial version, testing faker_clickstream module.
 - Batch producer; generates 10 clickstream "events" representing one user session and produces to a local Kafka cluster.


clickstream2.py
 - Stream producer; continuously produces user sessions in the form of 1 - 25 clickstream event records. Gracefully shuts down on keyboard interrupt (Ctrl+C).


clickstream3.py 
- Stream producer with identical behavior as clickstream2.py.
- Registers as external application with Lenses platform via HTTP Post call on start-up
