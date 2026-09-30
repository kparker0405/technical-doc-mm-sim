## 16. Development Mode
Development mode is configured in content.json.

**Development mode enabled**

When DevelopmentMode = TRUE, maintainers may see:
* Score totals
* Configuration versions
* Current QID and NodeKey
* Selected choice position
* Assigned curveball IDs
* Curveball category
* Final score thresholds
* Technical diagnosticc messages

**Development mode disabled**

When DevelopmentMode = FALSE, students see:
* Narrative content
* Decision questions
* Decision logs
* Recaps
* Curveballs
* Final outcome

They do not see internal scoring or technical details.

## 17. Release-Schedule Methodology
Levels are released according to this schedule:
|Level| Unlocked data/time| Time zone|
|---|---|---|
|2| [Date/time] | America/Detroit|
|3| [Date/time] | America/Detroit|
|4| [Date/time] | America/Detroit|

Release logic uses the Google Apps Script server time.

Development mode bypasses release restrictions.

**Checkpoint behavior**

Before release:
* The next level remains inaccessible.
* Students see the planned release time.
* Students may close the response and return later.

After release:
* The next level becomes available.
* Configuration files are refreshed.
* The next recap and curveball are displayed.

## 18. Content-Management Workflow
### 18.1 Editing scores
1. Open the scoring workbook
2. Edit the Scores sheet.
3. Export or save scores.csv.
4. Run the R conversion script.
5. Generate a new scores.json.
6. Upload it to the Qualtrics Files Library.
7. Update the preload URL if the file URL changed.
8. Begin a fresh test response.
9. Verify the displayed configuration version.
10. Publish the survey.

### 18.2 Editing curveballs or archetypes
1. Edit the curveballs.csv, archetypes.csv, or settings.csv. 
2. Run the content-conversion script.
3. Generate a new content.json.
4. Upload it to the Qualtrics Files Library.
5. Update the file URL if necessary.
6. Test curveball and display endings.
7. Publish the survey.

### 18.3 Editing the release schedule
1. Edit the release schedule Google Sheet. 
It will automatically update. 

### 18.4 Versioning convention
Recommended version format:

YYYY-MM-DD-HHMMSS

Record production versions here:
|Date|Survey version|Scores version|Content version|Editor|Summary|
|--|--|--|--|--|--|
|[Date] | [Version] | [Version] | [Version] | [Name] | [Change] | 
