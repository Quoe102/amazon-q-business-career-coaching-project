**What’s in this repo**

**Amazon Q Business – Project – Tobi Ogunmokun.pdf**

All screenshots with labels: IAM group setup, S3 data source, ACL path, blocked keywords, and successful/denied access tests.

**to-access-control.json**

The ACL configuration used to restrict the Medicine folder to approved coaches.

**How the app works**

**Upload inputs**

Learner CV

Job description

**Skill Gap Analysis**

Q compares the CV to the job description and lists missing skills.

**Training Recommendations**

Suggests 4–10 courses from the indexed catalog (S3 PDFs).

Considers anything the coach types in Recommendation by Coach (e.g., special focus, time limits).

If the field is blank, the app still runs normally.

**Schedule**

Builds a learning plan using available hours and preferences.

**Security and moderation**

**Access Control**

Only users in the CareerCoaches IAM Identity Center group can use the app.

The to-access-control.json file limits who can see content inside Medicine/ (denied) and allows Security/ (allowed).

Keyword blocking

Global controls block words like Gambling, Casino, and Self-harm from appearing in any recommendations.

**Keeping data current**

New course PDFs can be added to the S3 bucket.

The data source is scheduled to sync weekly, so updates appear automatically in the app.

**How to use or extend it**

Sign in as a coach from the CareerCoaches group and open the web link created by Amazon Q Business.

Upload a CV and job description, then follow the cards from top to bottom.

Optional: type extra guidance (specialty, hours, preferred format) into Recommendation by Coach to further tailor suggestions.

_Note: This project runs inside a private AWS environment (Udacity/AWS Scholars training account).
The code and configuration files here show how it was built, but the live Q Business app is not publicly accessible._
