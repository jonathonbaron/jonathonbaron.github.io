---
title: Checklist for the use of MTurk and Qualtrics Survey Methods
author: Jonathon Baron & Molly Offer-Westort
date: 2016-12-20
---
1. *Pre-planning: all survey experiments to be carried out on MTurk using Qualtrics must first proceed through several pre-planning stages.*
    (a) Presentation/discussion -- a draft of the survey instrument(s) must be presented before a senior colleague or professor
    (b) IRB exemption/approval -- following presentation workshopping, the amended instrument(s) must receive IRB exemption/approval
    (c) Preanalysis plan -- the exempt/approved project must then be detailed in a preanalysis plan to be hosted online prior to the collection of any data
2. *Qualtrics design: the survey, hosted on Yale's Secure Qualtrics platform, must satisfy several design requirements and pass associated checks before it can be launched.*
    (a) Independent confirmation -- prior to "alpha testing" with research assistants or lab members, confirm that the survey satisfies the following requirements, or has the following features
        i. Proper proofing and language requirements
            A. Complete thorough spelling and grammar checks
            B. Ensure that questions are worded appropriately, succinctly, and understandably
            C. Ensure that questions aim at the proper inferential target
            D. Ensure that question answer choices measure outcomes appropriately and succinctly
            E. Ensure that questions are formatted efficiently and readably, and reformat where appropriate (e.g., by condensing separate questions into a Matrix Table format)
            F. For all cases in which the researcher is uncertain about the correct solution to issues with items B - E in Section 2(a)i, randomization should be employed
        ii. Proper Survey Flow
            A. Randomization
                * Do *not* select "Evenly Present Elements"
                * *Do* ensure that the correct number of elements is set to be presented by the randomizer
                * Ensure that other design features (e.g., branching) remain constant across arms, where appropriate
            B. Branching
                * Ensure that branching is specified correctly (e.g., where conditional on embedded data, randomization)
                * In the case of random assignment into a given treatment via branching, ensure that arms do not appear sequentially
            C. Embedded data
                * Set embedded data at the beginning of the survey flow (i.e., prior to specifying other elements, *except* for Web Service elements for generating end-of-survey confirmation codes)
                * Confirm that terms are defined properly within the Survey Flow
                * When using piped text, confirm that terms are "called" correctly within survey question text
                * Where appropriate, confirm that embedded data selection is properly randomized
            D. End of Survey logic
                * Ensure that End of Survey logic is applied appropriately to end the survey when subjects do not meet recruitment requirements (e.g., consent, age, etc.)
        iii. Miscellaneous survey features and settings
            A. A consent form {\it must} be included as the first question
            B. An end-of-survey message containing randomized confirmation code *must* be specified in the survey
                * Ensure that the confirmation code is only generated for subjects who meet recruitment requirements (the default end-of-survey message may be used otherwise)
                * This message must be written in the Qualtrics Library, and specified in Survey Options
                * For additional confirmation, see Sections 2(a)ii.C. and 2(b)i
            C. Anonymization
                * Survey responses must be anonymized in accordance with IRB exemption/approval
            D. "Covariate" questions
                * For all covariate questions with appropriate analogues in the MTurkES survey instrument, use the MTurkES specification
            E. Follow-up surveys
                * Follow-up surveys *must* include either or both of the following elements, in confirmed working order
                    * An IRB-exempt/approved question or questions for matching respondents between waves
                    * Data collection enabling matching between waves
            F. Validation
\begin{itemize}
                * Ensure that each question features appropriate validation using Validation Options (e.g., Request Response, or Custom Validation for various input formats)
    (b) Alpha testing -- prior to "beta testing" with research assistants or lab members, the survey must be "alpha tested" in its entirety both using the Preview Survey functionality, and with recorded responses (using the Anonymous Link for web distribution)
        i. Independent testing (Preview Survey)
            A. Complete thorough independent testing procedures through the Qualtrics Preview Survey functionality; ensure that randomization, embedded data, and branching function correctly
        ii. Research-assistant testing (Preview Survey)
            A. Share survey with research assistants for a full, thorough review of instrument text and Survey Flow (including all survey elements)
            B. Ensure that research assistants complete a full, thorough review of the survey via the Preview Survey functionality
            C. The survey should contain stable, functioning elements as detailed in Section 2(a)
        iii. Independent testing (recorded responses)
            A. After ensuring that the survey functions as intended via instrument, Survey Flow, and Preview Survey review, generate an Anonymous Link for recorded responses
            B. Ensure that survey functionality is maintained with recorded responses
                * Attempt to "break" the survey functionality, especially with conditional embedded data, validation, and input text
                * Examine potential issues and data structure by downloading data via Data & Analysis (using legacy format)
        iv. Research-assistant testing (recorded responses)
            A. Share the Anonymous Link for recorded responses with research assistants for a full and thorough test of all survey features and functionalities
                * Instruct research assistants to attempt to "break" the survey functionality, especially with conditional embedded data, validation, and input text
                * Examine potential issues and data structure by downloading data via Data & Analysis (using legacy format)
    (c) Beta testing -- when conducting research as part of a research lab, surveys must be "beta tested" with lab members using the Anonymous Link for web distribution (following independent and research-assistant "alpha testing")
        i. Instruct lab members to attempt to "break" the survey functionality, especially with conditional embedded data, validation, and input text
        ii. Where employing randomization, request that lab members record which treatment(s) they receive, to confirm proper randomization
        iii. Examine potential issues and data structure by downloading data via Data & Analysis (using legacy format)
3. *MTurk HIT specification: once the Qualtrics survey is in concordance with the checklist items enumerated in Section 2, an MTurk HIT must be created and designed appropriately.*
    (a) Create a new HIT
        i. Navigate to the "Create" tab at the navigation bar at the top of the MTurk Requester page
        ii. If not employing an MTurk default format, select "Other" from the format list on the left; then select "Create Project"
        iii. Specify requirements for "Describe your HIT to Workers"
            A. Specify a "HIT Title"
            B. Specify a short "HIT description"
            C. Specify appropriate "Keywords" pertaining to the HIT
        iv. Specify requirements for "Setting up your HIT"
            A. Specify "Reward per assignment" (i.e., the payment rate, per subject)
            B. Specify "Number of assignments per HIT" (for a survey or survey experiment, this will correspond to the number of subjects to be recruited for the pilot or study---see Section 4(a) for further details; $.50/5 minutes is recommended)
            A. Specify "Time allotted per assignment" (1 Hours is recommended as a default)
            B. Specify time for "HIT expires in" (5 Days is recommended as a default)
            C. Specify time for "Auto-approve and pay Workers in" (8 Hours is recommended as a default)
        v. Specify "Worker requirements"
            A. *Do not* "Require that Workers be Masters to do your HITs
                * Masters are not required for quality tasks, but cost appreciably more than standard MTurk workers
            B. "Specify any additional qualifications Workers must meet to work on your HITs" (up to five may be set)
                * Set "Location is UNITED STATES (US)," or other location as appropriate and exempt/approved by IRB
                * "HIT Approval Rate (\%) for all Requesters' HITs greater than or equal to 95," or a different threshold as appropriate for the task (a higher HIT Approval Rate is recommended for higher-quality responses)
                * "Number of HITs Approved" to "greater than or equal to 50"
                * Specify whether the "Project contains adult content"
                * Set "HIT Visibility" to "Hidden" - Only Workers that meet my HIT Qualification requirements can see and preview my HITs
            C. For follow-up Surveys
                * Remove "HIT Approval Rate" and "Number of HITs Approved" qualifications
                * Include additional qualification type based on Worker ID collected in the preceding wave(s)
                    * Qualifications can be assigned using `MTurkR`, which may also be used to recontact workers
                    * When recontacting workers, save the recontact output email text with other data files

        vi. Specify Design Layout
            A. Paste and format study description into the "Design Layout" (the appended default format is recommended)
            B. Ensure that the Anonymous survey link URL directs subjects to the correct, live survey via the Anonymous Link noted in Sections 2.(b)iii - 2.(c)
            A. Ensure that respondents can specify the end-of-survey random confirmation code provided to subjects who complete the Qualtrics survey
4. *Launching the HIT: once the checklist items enumerated in Section 2, as well as the design specifications enumerated in Section 3 are fulfilled, the MTurk HIT can be created to recruit and pay subjects.*
    (a) Piloting -- the HIT *must* first be launched as a pilot study, including no fewer than 20 subjects recruited from MTurk, to ensure proper functionality in both MTurk and Qualtrics prior to distribution using a full sample
        i. Navigate back to the "Create" tab at the navigation bar at the top of the MTurk Requester page
        ii. Select "Publish Batch" to the left of the relevant "Project"
        iii. On the "Preview" page, confirm the following
            A. Confirm the accuracy of the Reward, HITs available, Duration, and Qualifications listed at the top of the page
            B. Confirm the format of the ``HIT Preview,'' and the accuracy of the Anonymous Link and survey code text box
        iv. On the "Confirm and Publish" page, confirm the following
            A. Confirm the accuracy of the Batch Properties
            B. Confirm the accuracy of the HITs specifics
            C. Confirm the accuracy of the Cost Summary
            D. Confirm the accuracy and sufficiency of Payment
                * Confirm the accuracy of the Payment Method
                * Where appropriate, if using funds from an external source (e.g., from a faculty research account), confirm the status of the HIT and Qualtrics survey prior to the transfer of relevant funds
                    * Funds should match the quoted Balance Due exactly
            E. Once all aspects of the HIT are confirmed, select "Purchase & Publish"; the HIT's progress may now be monitored by navigating to the "Manage" tab at the navigation bar at the top of the MTurk Requester page
        v. Confirm the validity of the pilot study using Qualtrics and MTurk data (the latter of which can be accessed via Manage &rarr; Results) and potential MTurker feedback, and correct any remaining errors
    (b) Full distribution -- once the pilot study has been completed and accuracy of all design elements and data are confirmed, the study may be distributed to the entire subject pool
        i. Given a flawless pilot study, launch the HIT following the relevant instructions in Section 4(a), on $n - k$ subjects, where $n$ refers to the total number of subjects targeted for the study, and $k$ refers to the number of subjects included in the pilot
            A. Subjects from the pilot stage must be excluded using a new qualification type (which can be assigned in \verb+MTurkR+)
        ii. Given the unlikely possibility of a problematic pilot study, the researcher must correct all apparent errors; depending on the severity, the researcher may choose to proceed according to one of the following approaches
            A. Re-pilot the study, using a separate pilot group
            B. Proceed according to Section 4(b)i
            C. Proceed by relaunching the HIT with $n$ subjects
                * The relaunched HIT should exclude the $k$ subjects from the flawed pilot study
