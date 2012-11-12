This is the source and associated files for the edX MITx 6.00x course's Problem Set 6. It is an application that reads the RSS feeds from Google News and Yahoo News and filters the stories according to triggers defined in the triggers.txt file. The ps6.py is primarily my own work, although parts of it were prewritten by course staff (mostly marked as "helper code" or similar in the comments). I take no credit for feedparser.py (provided by feedparser.org) or project_util.py (provided by MIT staff). I have included them here so that ps6.py will run correctly.

The format for triggers in the trigger file is `<name> <TYPE> <parameters>`. For example, to define a trigger named t1 that searches the titles of news items for the word "hurricane", I would enter this line in triggers.txt: `t1 TITLE hurricane`. Here are the valid values for `<TYPE>`:
<table>
  <tr>
    <th>TYPE</th><th>Searches</th><th>Valid Parameters</th>
  </tr>
  <tr>
    <td>TITLE</td><td>titles</td><td>one word, case-insensitive</td>
  </tr>
  <tr>
    <td>SUBJECT</td><td>subjects</td><td>one word, case-insensitive</td>
  </tr>
  <tr>
    <td>SUMMARY</td><td>summary snippets</td><td>one word, case-insensitive</td>
  </tr>
  <tr>
    <td>PHRASE</td><td>titles, subjects, and summaries</td><td>any number of words, case-sensitive and in that order</td>
  </tr>
  <tr>
    <td>NOT</td><td>per parameter trigger</td><td>the name of another trigger whose results should not be displayed</td>
  </tr>
  <tr>
    <td>AND</td><td>per parameter triggers</td><td>two names of other triggers, both must fire to display story</td>
  </tr>
  <tr>
    <td>OR</td><td>per parameter triggers</td><td>two names of other triggers, one or both of which must fire to display story</td>
  </tr>
</table>