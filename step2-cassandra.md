<!-- TOP -->
<div class="top">
  <img class="scenario-academy-logo" src="https://datastax-academy.github.io/katapod-shared-assets/images/ds-academy-2023.svg" />
  <div class="scenario-title-section">
    <span class="scenario-title">Exercise 3.1: User Defined Types (UDTs)</span>
    <span class="scenario-subtitle">ℹ️ For technical support, please contact us via <a href="mailto:academy@datastax.com">email</a>.</span>
  </div>
</div>


<!-- NAVIGATION -->
<div id="navigation-top" class="navigation-top">
 <a href='command:katapod.loadPage?[{"step":"step1-cassandra"}]'
   class="btn btn-dark navigation-top-left">⬅️ Back
 </a>
<span class="step-count"> Step 2 of 4</span>
 <a href='command:katapod.loadPage?[{"step":"step3-cassandra"}]' 
    class="btn btn-dark navigation-top-right">Next ➡️
  </a>
</div>

<!-- CONTENT -->

<div class="step-title">Create a keyspace and table</div>

✅ Start the CQL shell:
```
cqlsh
```

✅ Create a keyspace called `killrvideo` and switch to that keyspace. Use `NetworkTopologyStrategy` for the replication class and set the replication factor of `1` for datacenter `DC-Houston`. Remember the `USE` command switches keyspaces.
```
CREATE KEYSPACE IF NOT EXISTS killrvideo
WITH replication = {
  'class': 'NetworkTopologyStrategy', 
  'DC-Houston': 1 };

USE killrvideo;
```

✅ Create the original table `videos`:
```
    CREATE TABLE videos (
       video_id TIMEUUID,
       added_date TIMESTAMP,
       description TEXT,
       tags SET<TEXT>,
       title TEXT,
       user_id UUID,
       PRIMARY KEY (video_id)
     );
```


<!-- NAVIGATION -->
<div id="navigation-bottom" class="navigation-bottom">
 <a href='command:katapod.loadPage?[{"step":"step1-cassandra"}]'
   class="btn btn-dark navigation-bottom-left">⬅️ Back
 </a>
 <a href='command:katapod.loadPage?[{"step":"step3-cassandra"}]'
    class="btn btn-dark navigation-bottom-right">Next ➡️
  </a>
</div>
