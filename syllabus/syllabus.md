# Spatial Programming (GEOG 49076 / 59076 / 79076)

Kent State University

College of Sciences and Humanities

Department of Geography

Fall 2026 (SIS ID: 13481.202680)

## Class meetings

Room: 442 McGilvrey Hall

Meetings: Tu/Th: 12:30–1:45pm

## Instructor

Dr. Patrick Bitterman

Office: 436 McGilvrey Hall

Email: <pbitterm@kent.edu>

Office hours: Tuesday and Thursday, 10:30am–12:00pm

## Department Chair

Dr. Sarah Smiley

Office: 413D McGilvrey Hall

Email: <ssmiley8@kent.edu>

---

## Course description

This course teaches the fundamentals of programming and scripting to automate and standardize geospatial analysis and data management. Using the Python programming language, this course teaches students to design clearly structured programs and introduces both open source tools and the ArcPy library to access ArcGIS Pro geoprocessing tools. Students will develop algorithms and programs to edit, query, manipulate, and analyze spatial data. Students will also build scripts, tools, and small programs; work with a range of spatial data formats; practice reading and reviewing other people's code; generate graphical output (maps and other plots); and create reproducible workflows. Students will integrate these methods with ArcGIS and the Python programming language.

## Prerequisites

Students are expected to have completed GEOG 49070: Geographic Information Science or similar course.

Previous programming experience is not required, but is helpful.

## Learning objectives

By the end of the term, you will be able to:

1. Automate geospatial data management and analysis tasks with Python, both inside ArcGIS Pro (via arcpy) and using open-source libraries
2. Select appropriate spatial data formats (e.g., shapefile, file geodatabase, GeoPackage, GeoParquet, raster formats) for a given task, and explain the tradeoffs behind that choice
3. Analyze workflows and describe code and algorithms in plain language, including reading and adapting scripts someone else wrote
4. Design and build small, reusable programs and tools (e.g., functions, script tools, toolboxes) that interface with GIS software
5. Conduct and respond to code review: give specific, professional feedback on a peer's code, and revise your own work in response to feedback you receive
6. Use AI coding assistants critically — treat generated code as a draft to verify, test, and understand, not a finished answer you submit unread
7. Plan, develop, and execute an independent programmatic analysis of a dataset, and communicate the results clearly

## Materials

All readings are free and linked from Canvas or the course repository

All software and tools used in this course are free to you:

- **ArcGIS Pro** is available via KSU institutional access
- **Google Colab** requires only a free Google account
- **GitHub** requires only a free account

See the account setup guide in the course repository for step-by-step sign-up instructions for GitHub and Google/Colab.

If you want to work outside the lab, ArcGIS Pro only runs on Windows; the open-source portion of the course will run entirely in the browser via Colab, so it works on any machine with an internet connection.

---

## Assessment

| Component | Points | Grading mode |
|---|---|---|
| Labs 1–8 (8 × 75 points) | 600 | Rubric-graded |
| Practicums 1–2 (2 × 100 points) | 200 | Rubric-graded |
| Sketches (6 × 25 points) | 150 | Completion-graded |
| Participation | 50 | Holistic |
| **Total** | **1000** | |

### Labs

There are 8 lab assignments across the semester. Labs become more complex and less guided as the semester progresses. Every lab "ships" with a student template notebook. You *MUST* use it for your submission. Due dates are listed on the course schedule; submit all labs through Canvas.

**Lab 8**, due finals week, is a fully-scoped take-home synthesis lab in Colab — the instructor sets the dataset and analytical brief; you make the analytical choices within that scope. It closes out Part 2 in place of a traditional final project. **Graduate students** complete additional documentation requirements on Lab 8 and a related memo — see the Graduate Research Thread below.

### Sketches and peer review

Sketches are short, low-stakes exercises designed to take about 45–75 minutes to complete, that reinforce that week's material. There are 6 sketches across the semester, each worth 25 points, split:

- **15 points** for submitting your sketch on time (this includes the stretch task, as part of what counts as "complete")
- **10 points** for completing your assigned peer review(s) on time

Sketches are completion-graded, not rubric-graded: submitting a good-faith, on-time attempt earns full credit for that half. There is no partial credit for lateness or incompleteness beyond the policy below.

After each sketch deadline, Canvas automatically assigns you one classmate's submission to review, using a fixed three-prompt form: 1) what does this code do well, 2) where would it break or mislead, and 3) one concrete improvement.

Peer review in this course is **attributed, not anonymous**, meaning your name is visible to the person you review, and theirs is visible to you. Treat the process like professional code review: direct, specific, and useful, aimed at the code rather than the person. This is training for the kind of feedback you'll give and receive in any collaborative programming environment.

### Practicums

Each part of the course ends in a two-day, in-person, **paired-programming practicum**. Each is worth 100 points and is rubric-graded:

| Component | Points |
|---|---|
| Design artifact (Tuesday) | 40 |
| Working implementation + tests (Thursday) | 50 |
| Professionalism | 10 |

**Tuesday** is planning and architecture: with your partner, you will produce a paper design artifact. **Thursday** you will implement and test what you designed, under observation, and submit a runnable notebook with evidence that you tested it.

Documentation and your own course notes and notebooks are acceptable, but no AI-generated code, completions, or explanations.

Pairs are **assigned by the instructor and will rotate** each practicum, drawn from your sketch peer-review pairings. If you must miss a practicum day, contact the instructor as soon as possible to arrange a make-up.

### Participation (50 points)

Participation is graded holistically based on engagement in class. For example, asking questions, contributing to discussion, and being present and attentive during lab and lecture time.

---

## Graduate Research Thread

This course is offered at three levels: GEOG 49076 (undergraduate), GEOG 59076 (Master's), and GEOG 79076 (doctoral). Students enrolled in 59076 and 79076 are "graduate students" for the purposes of the requirements below. Sketches, practicums, and participation are the same for both. The differentiation is a **Graduate Research Thread**: three short memos that translate the course's skills onto your own research, each attached to a specific lab.

- **Memo 1 — Automation scoping**, due with Lab 3: identify a repetitive data task in your own research domain; write an inputs/outputs spec and pseudocode for automating it
- **Memo 2 — Data audit + methods critique**, due with Lab 5: audit a dataset relevant to your research, and critique the methods of a published study that tackled a similar spatial programming problem
- **Memo 3 — ESDA pilot + notebook**, due with Lab 8: a small exploratory spatial data analysis pilot on your own data, including an extended interpretation section — situating the analysis in relevant literature and critically evaluating methodological choices, limitations, and possible extensions

Each memo is **1–2 pages** and is graded as a **10-point "graduate component"** criterion inside that lab's graduate rubric variant. 

**If you do not yet have a defined research topic** (e.g., you're early in a program, or between projects), use a data or automation question from your home program that you are genuinely considering. Memos are meant to make the course's skills useful to your own work, not to require a finished thesis question.

On **Lab 8**, graduate students also prepare deeper code documentation: inline comments explaining analytical decisions, a README describing the workflow and dependencies, and clear annotation of data sources — sufficient for an independent reader to reproduce your work.

---

## Course policies

### Late work

Unless otherwise noted for a specific assignment:

- All assignments are due on the date specified in the course schedule and assignment instructions
- Late work is accepted but penalized 20% of the potential points for each day it is late

### Changes to the syllabus

Any changes to this syllabus will be communicated by email and posted on the Canvas course page.

### Working in the lab

You are free to work in the GIS lab whenever it is open and not in use by another class; be respectful of other classes using the space. Digital file storage on lab computers should always be treated as temporary — save each lab in its own directory and sync your work to GitHub or another backup location regularly. You are always responsible for your own data.

### Collaboration

While you may choose to interact with other students on laboratory assignments and the final project, all submitted work is expected to be your own. All write-ups, discussion statements, and other work should be your own, individual thoughts. Your maps, labs, sketches, and practica should also reflect work that is independent and unique to you.

Students who do not follow these policies will be reported to the College for academic dishonesty. If you have questions regarding this policy, it is your responsibility to ask them.

### Your Responsibilities
You have a responsibility to help create a classroom environment where all may learn. At the most basic level, this means you will respect the other members of the class and the instructor and you will treat them with the courtesy you expect to receive in return. This policy applies to all forms of communication in this course. Any email correspondence will be conducted via your Kent State email address.

### Miscellany
Be honest and have integrity in your work. For example, do not increase the perceived length of a lab report by increasing the size of punctuation or manipulating spacing. Be kind and be polite. Finally, you will get out of this class what you put into it – be prepared, participate, and be attentive, and you will be successful.

---

## Grading scale

| Grade | % | Grade | % | Grade | % | Grade | % |
|---|---|---|---|---|---|---|---|
| A | 94–100 | B+ | 87–89 | C+ | 77–79 | D+ | 67–69 |
| A- | 90–93 | B | 84–86 | C | 74–76 | D | 64–66 |
| | | B- | 80–83 | C- | 70–73 | D- | 60–63 |
| | | | | | | F | Below 60 |

### Extra credit

Extra credit assignments and opportunities are not offered

---

## Course schedule

See the course schedule on *Canvas* for the week-by-week topics, readings, and due dates for labs, sketches, peer reviews, and the practicums


## University policies

### Request for Religious Accommodations
The University welcomes individuals from all different faiths, philosophies, religious traditions, and other systems of belief, and supports their respective practices. In compliance with University policy and the Ohio Revised Code, the University permits students to request class absences for up to three (3) days, per semester, in order to participate in organized activities conducted under the auspices of a religious denomination, church, or other religious or spiritual organization. Students will not be penalized as a result of any of these excused absences.

The request for excusal must be made, in writing, during the first fourteen (14) days of the semester and include the date(s) of each proposed absence or request for alternative religious accommodation. The request must clearly state that the proposed absence is to participate in religious activities. The request must also provide the particular accommodation(s) you desire. 

You will be notified by me if your request is approved, or, if it is approved with modification. I will work with you in an effort to arrange a mutually agreeable alternative arrangement. For more information regarding this Policy you may contact the Student Ombuds (<ombuds@kent.edu>).

### Course registration and withdrawal
The official registration deadline for this course is January 18th.  University policy requires all students to be officially registered in each class they are attending. Students who are not officially registered for a course by published deadlines should not be attending classes and will not receive credit or a grade for the course. Each student must confirm enrollment by checking his/her class schedule (using Student Tools in FlashLine) prior to the deadline indicated.  Registration errors must be corrected prior to the deadline. The course withdrawal deadline is March 29th.

### Student Accessibility Services Statement
Kent State University is committed to inclusive and accessible education experiences for all students. University Policy 3342-3-01.3 requires that students with disabilities be provided reasonable accommodations to ensure equal access to course content. Students with disabilities are encouraged to connect with Student Accessibility Services as early as possible to establish accommodations. If you anticipate or experience academic barriers based on a disability (including mental health, chronic medical conditions, or injuries), please let me know immediately.

### Basic Needs Support & Mental Health Well-being
Kent State University is committed to supporting the overall well-being of our students. This support may take the form of assisting students with basic needs such as food and housing. We recognize that the absence of secure housing and access to food makes it difficult for students to achieve their best in and out of the classroom. If you, or someone you know, are unable to afford groceries or lack a safe, secure, and reliable place to live, please visit the CARES Center basic needs resource website: <https://www.kent.edu/carescenter/basic-needs-resources>.

Mental health challenges may also make it difficult for students to reach their full potential. KSU’s mental health and wellness resource page provides information on education and awareness, mental health services, and advocacy intervention. To learn more, please visit Kent State’s mental health resources and support website at <https://www.kent.edu/mentalhealth>.

### Academic honesty
The Administrative Policy regarding student cheating and plagiarism (3-01.8)has been revised to include details on generative AI (GAI). The policy defines GAI as any internet-based generative artificial intelligence program that makes use of large language model algorithms to create content and that the use of GAI to generate content for assigned coursework, unless expressly permitted by the instructor in the syllabus or assignment instructions, is considered to be cheating.  <https://www.kent.edu/policyreg/administrative-policy-regarding-student-cheating-and-plagiarism>. 

### Disruptive student policy
I expect all people in this academic space will be respectful. If a person is disruptive, I will enforce university policy.

Examples of disruptive behavior may include but are not limited to:
•	Monopolizing class time with excessive comments or questions
•	Interrupting class sessions or assignments
•	Abusing faculty office hours
•	Repeatedly speaking in an elevated or angry/aggressive tone
•	Attacking the beliefs or conclusions others draw in class.

Please see KSU policy 4-02.2 and process for disruptive students, which include referral to the Office of Student Conduct as I deem necessary.

### Registration and records policy
Only students who have been formally admitted to Kent State University may register for coursework and pay the appropriate fees. An official registration is a record of the students’ approved schedule or classes maintained online in the university’s student information system. Students who are not officially registered for a course by published university deadlines should not attend classes and will not receive credit or a grade for the course.

### Kent Campus Academic Support Statement
Kent State recognizes many students face challenges and we are committed to supporting your academic journey when you need help.  Please check out these resources to help as you build your support system:
- What is the first step I should take to get academic support for this class?
    - Reach out to your instructor!
- Where can I get help from another student who earned a good grade in this class?
    - [Tutoring](https://www.kent.edu/asc/univ-tutoring)
- Where can I go if I need assistance with how to study and meet my academic goals?
    - [Academic Coaching](https://www.kent.edu/coaching)
- Who can review my writing and help me properly cite my work?
    - [Writing Commons](https://www.kent.edu/writingcommons)
- Where should I go when I don’t know where to go?
    - [Academic Advising](https://www.kent.edu/university-advising)
    - [TRIO Student Support Services](https://www.kent.edu/studentsupportservices)

There may be additional resources, just ask
