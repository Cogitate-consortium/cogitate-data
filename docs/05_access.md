# Access to COGITATE Data

There are two ways of accessing the COGITATE data:

1. "Live" Database Release: [XNAT](https://wiki.xnat.org/documentation/) (eXtensible Neuroimaging Archive Toolkit)
2. Archival Format: Bundles

<table>
    <tr>
        <td>
            <a href="">
                <img
                    src="https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.0/graphics_v1.0/xnat.png"
                    width=""
                    alt="alt_text"
                    title="XNAT login page"
            /></a>
        </td>
        <td>
            <a href="https://www.arc-cogitate.com/data-bundles-active">
                <img
                    src="https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.0/graphics_v1.0/bundles.png"
                    width=""
                    alt="alt_text"
                    title="Data bundles login"
            /></a>
        </td>
    </tr>
</table>

<span style="background-color: #ffc7c7"><strong>NOTE: XNAT release not available yet!</strong></span>

## 1. XNAT

This database offers a web interface for navigating the data and an API (Application Programming Interface) for programmatically retrieving specific databases based on user interests. Comprehensive instructions on how to register, access, and query our database are provided below.

### **Step 1: Registration**

If you are a new user and have not registered yet, you should visit [Cogitate_XNAT_registration](https://cogitate-data.ae.mpg.de/app/template/Register.vm#!). Once the registration is done, a verification step, the same as the “Creating an Account”, is needed.

If you have already registered, you can skip this step and login at [Cogitate_XNAT](https://cogitate-data.ae.mpg.de/app/template/Login.vm#!).

![alt_text](https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.0/graphics_v1.0/xnat_user_login.png "XNAT User Login Page")

### **Step 2: Navigating at XNAT**

After completing the registration step, you can log in with your User and Password. You can see the list of available datasets under the “Projects” tab.

![alt_text](https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.0/graphics_v1.0/xnat_projects.png "XNAT Projects page")

Once you click the project’s name, you will see the list of subjects in the farthest left column.

![alt_text](https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.0/graphics_v1.0/xnat_meg_subjects.png "XNAT Subjects page")

In each subject’s folder, the demographic information of that subject and the various sets of data acquired for Experiment 1 are provided. As an example, for a subject with the ID of CA103, the MR session, Eye tracker and MEEG datasets are listed as the below figure.

![alt_text](https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.0/graphics_v1.0/xnat_meg_subject_folder.png "XNAT Subject folder")

In the MR session folder, you can view and access the MR scan of the subject along with the related imaging parameters.

![alt_text](https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.0/graphics_v1.0/xnat_meg_MR-anat.png "XNAT MR Anatomical Scan Folder")

![alt_text](https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.0/graphics_v1.0/xnat_meg_MR-scan-pic.png "XNAT MR Example")

In the Eye tracker folder, the eye tracking data of different runs and some details related to them, including the recorded eye, sampling frequency, distance to screen and screen size are available.

![alt_text](https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.0/graphics_v1.0/xnat_meg_eyetracker-scan-DurR1.png)

Under the folder of MEEG, there are some tabs on the top where you can find information regarding the Case Report Form, Exit Questionnaire, experiment checklist form, data details within the BIDS framework, and at the bottom, you can download different runs of MEG data.

![alt_text](https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.0/graphics_v1.0/xnat_meg_upload_form.png)

![alt_text](https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.0/graphics_v1.0/xnat_meg_meg-data.png)

### Naming Convention on XNAT

The data on XNAT is organized into subjects and sessions under a given project. The subjects are identified using the format “CX???” and the sessions follow the format CX???_MODALITY_VISIT_PARADIGMRUN e.g. CA103_MEEG_1_DurR1 indicated MEEG measurement for subject ID CA103 during the first visit with Dur experimental paradigm run 1 (R1).

## **2. Bundles**

This approach involves providing a collection of links to the prepared bundles of the data and accompanying metadata, which are available in zip format. These links grant users the ability to download specific modalities, example datasets, or the complete dataset.

![alt_text](https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.0/graphics_v1.0/bundles_sample_datasets.png "Bundles Sample Datasets")

![alt_text](https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.0/graphics_v1.0/bundles_full_datasets.png "Bundles Full Datasets")

Here is a brief explanation about how to access the data bundles:

### Step 1: Create a Data User Account

<p>
    <a href="https://www.youtube.com/watch?v=FFqN5Pech0w"
        ><img
            src="https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.0/graphics_v1.0/youtube_logo.png"
            alt="alt_text"
            title="image_tooltip"
            width="20"
            height="15"
    />
    <strong>Step 1: Create a Data User Account</strong>
</p></a>

Access to the data bundles requires a quick and easy registration process.

1. Provide user information, including name and email address.
2. Read and accept the [Terms of Use](https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.0/linked_files_v1.0/Cogitate_ToU_v1.pdf) and [GDPR Requirements](https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.0/linked_files_v1.0/Cogitate_GDPR_v1.pdf) ([General Data Protection Regulation](https://gdpr-info.eu/)).
3. Once you register, you will receive four (4) emails to the email account you registered with. In some cases, checking your junk mail may be necessary.
    1. **_Welcome email_**: general information
    2. **_Data User Account Verification email:_** Within the verification email, you must click on the ‘verify my account’ option to finalize step 1 of creating a data user account in order to gain access to all current and future data releases.
    3. **_Resource Material_**: A handy email that contains all the important links that serve as reference materials to Cogitate data.
    4. **_Mailing List Subscription:_** In order to stay up-to-date and informed about news related to COGITATE data releases, you must activate your email subscription (this is in compliance with GDPR requirements).

<span style="background-color: #ffc7c7"><strong>Tip:</strong> The registration procedure needed for accessing the data bundles is a separate step than what is required to access XNAT.</span>

### Step 2: Login and logout of your Data User account

<p>
    <a href="https://www.youtube.com/watch?v=6BR3uYqiDiU"
        ><img
            src="https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.0/graphics_v1.0/youtube_logo.png"
            alt="alt_text"
            title="image_tooltip"
            width="20"
            height="15"
    />
        <strong>Step 2: Login and logout of your Data User account</strong>
</p></a>

1. To **<span style="text-decoration:underline;">login</span>** to your account, go to the Login button on the top right of the page. Enter your email and password used when registering. You should now have access to the Cogitate Data User main page and Data Bundles.
2. To **<span style="text-decoration:underline;">log out</span>** of your account, go to the top navigation bar and hover of Data. In the dropdown menu, click on Data User Account. A panel will open on the right side of the screen - click on Account Settings in the bottom of that panel. Then the option to Sign out will appear under your username. Click on Sign out.

<span style="background-color: #ffc7c7"><strong>Tip:</strong> The Login button will remain as 'Login' even after signing in to your account. The only way of knowing whether you are logged in or out, is by clicking on Data User Account, under the Data heading or being able to download data (i.e. indicating you are in fact, logged in)</span>

<p>
    <a href="https://youtu.be/KraiX4ttE2o"
        ><img
            src="https://github.com/Cogitate-consortium/cogitate-data/raw/main/assets/documentation_v1.0/graphics_v1.0/youtube_logo.png"
            alt="alt_text"
            title="image_tooltip"
            width="20"
            height="15"
    />
        <strong>Step 3: How To Download the Data</strong>
</p></a>

1. Login to your account
2. Scroll down and click on the “Access Data Bundles”
3. Click on the download button next to each dataset

### Naming Convention for Bundles

Raw data bundles follow the below naming convention. The project root directory consists of subdirectories named after the subject's ID which is of the format “CX???”. The subject directories consist of various sub directories as described below. Except for the metadata directory the sessions follow the pattern subject-ID_PARADIGM_MODALITY. If the modality data is paradigm agnostic, e.g. MR, CT then the paradigm is left blank.

We currently have two paradigms in the data EXP1 indicating the experiment described and FingerLoc for the finger localiser. The session directories further contains individual scans following the format CX???_MODALITY_1_DurR1.EDF.

The metadata subdirectory further consists of various assessments and questionnaires that provide valuable information.
