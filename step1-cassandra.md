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
 <a href='command:katapod.loadPage?[{"step":"intro"}]'
   class="btn btn-dark navigation-top-left">⬅️ Back
 </a>
<span class="step-count"> Step 1 of 4</span>
 <a href='command:katapod.loadPage?[{"step":"step2-cassandra"}]' 
    class="btn btn-dark navigation-top-right">Next ➡️
  </a>
</div>

<!-- CONTENT -->

<div class="step-title">Explore the KillrVideo dataset</div>


After reviewing your design of the tables that support tag and year queries, your manager happened to remember that there isn't a `tags` column in the original table that stores video metadata. You have now been asked to include that in the videos table schema and also to add another column to store video encoding information.

The revised `videos` table schema:

| Column Name      | Data Type |
|------------------|-----------|
| video_id         | timeuuid  |
| added_date       | timestamp |
| description      | text      |
| encoding         | video_encoding |
| tags             | set<text> |
| title            | text      |
| user_id          | uuid      |

<br/>

The encoding data structure:

| Column Name      | Data Type |
|------------------|-----------|
| bit_rates        | set<text> |
| encoding         | text      |
| height           | int       |
| width            | int       |

<br/>


✅ Review the contents of the CSV files with video metadata:
```
head -n 10 assets/videos.csv
```

```
head -n 10 assets/videos_encoding.csv
```

<!-- NAVIGATION -->
<div id="navigation-bottom" class="navigation-bottom">
 <a href='command:katapod.loadPage?[{"step":"intro"}]'
   class="btn btn-dark navigation-bottom-left">⬅️ Back
 </a>
 <a href='command:katapod.loadPage?[{"step":"step2-cassandra"}]'
    class="btn btn-dark navigation-bottom-right">Next ➡️
  </a>
</div>
