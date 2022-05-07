# ![logo](https://github.com/UIBat/UIBat/blob/main/UIBat-logol-1.png) 

# UIBat
An approach to automatically detect, localize, and repair the UI display issues in Android apps.<img style="width:40px" src="https://github.com/UIBat/UIBat/blob/main/UIBat-logol-2.png"> 

# UIBat Dataset (./UIBat/)

The dataset includes empirical study dataset and experimental application information. Please note that the effective evaluation dataset and useful evaluation dataset in our paper are from **real-world apps on GitHub (Every app can be retrieved)**. In this paper, we give information such as app name, issue ID, repair commit ID, etc. Researchers can find the corresponding data (APP information, APK, source code) by retrieving relevant information. Due to space constraints, we only give the relevant information of the app and no longer give the corresponding source code and APK.

(./Dataset/) shows the dataset of UI display issue we collected in our paper, it includes Android app screenshots of the UI display issue, screenshots of issue reports from Github, issue reports of Android apps in Github, issue report and its corresponding repair commit link. Please note that one of the **contributions** of this paper is to provide **datasets of Android UI issues**. So we update the dataset regularly. Therefore, the dataset provided here are **updated** datasets (**richer and larger** than those mentioned in this article).

We apologize for the issue caused by the size limit in GitHub. We update the information on GitHub and move dataset to the appropriate platform, Zenodo. **Because the dataset is too large**, GitHub is limited by the file upload size. And there is a file error in the previously uploaded data. In order to facilitate the download of researchers, we uploaded the corresponding data sets to the anonymous **Google Drive**. The sharing ***link of Google Drive*** is: https://drive.google.com/drive/folders/1NT8RrcxBR8PGw2tdEGriCaqgsfHN5tEW?usp=sharing

<!-- ![UIBat Data Drive](https://github.com/UIBat/UIBat/blob/main/dataset-googledrive.png) -->
<div align=center>
<img src="https://github.com/UIBat/UIBat/blob/main/dataset-googledrive.png" height="360px"/>
</div>

We are very sorry. Due to the large size of the dataset, we tried to transfer multiple Online Disk(e.g., Onenote, Google Drive), and there were upload errors. In view of this situation, we have developed corresponding web pages in **UIBat website** for our dataset. Please note that we update our dataset in real-time on our **UIBat website**, and the web page is shown in the figure below. Click "learn more" of dataset on UIBat to obtain the information of this dataset page.

![UIBat Dataset](https://github.com/UIBat/UIBat/blob/main/UI%20display%20issue%20dataset.png) 

In order to help you better understand, we give three types of UI display issues. As shown in the Figure, they have obvious **visual differences** and **image features**, so can be distinguished with computer vision technologies. 


## Pull Request (Usefulness Evaluation)

We further assess the usefulness of UIBat in real-world practice. 
UIBat detects 129 previously undetected UI display issues from the 106 apps, which again indicates the prevalence of UI display issues, and the necessity for the auto-repair. UIBat can repair 121 (94%) of them. 
For the 121 submitted pull requests, 92 of them are successfully merged by developers, while the remaining are still pending (none of them is rejected), as shown in Table

**No.** | **Commitid** | **APP Name** | **Category** | **Version** | **Download** | **Status**
 :-: | :-: | :-: | :-: |  :-: | :-: | :-: 
1 | 4345457 | PicardScanner| Media | 1.5 | 5K+ | Merged 
2 | eda6be6 | EVMap| Navig | 0.8.3 | 10K+ | Merged 
3 | 867b6e2 | Hendroid | Reading | 1.15.0 | 10K+ | Merged 
4 | 2907e19 | EinkBro| Reading | 8.12.1 | 5K+ | Merged 
5 | f34382f | EinkBro| Reading | 8.12.1 | 5K+ | Merged 
6 | 15e7434 | Notes| Writing | 1.17 | 5K+ | Merged 
7 | 8a76280 | AlarmClock| System | 3.09.01 | 1M+ | Merged 
8 | 37c437c | GPSLogger| Navig | 112 | 1M+ | Merged 
9 | 85b1ea7 | Commons | Internet | 3.0.3 | 50K+ | Merged 
10 | f4bab69 | Commons | Internet | 3.0.3 | 50K+ | Merged 
11 | 9fc20a2 | AutoClicker| System | 1.0-RC4 | 1K+ | Merged 
12 | ebc914c | Silence| Connect | 1.6.2 | 1K+ | Merged 
13 | 5fe47cf | OpenChess| Games | 1.9.5 | 1K+ | Merged 
14 | 5482728 | Syncthing| Internet | 1.18.0 | 1M+ | Merged 
15 | 458d704 | WebWeaver| Education | 0.3.0 | 1K+ | Merged 
16 | 5fcf8e1 | WebWeaver| Education | 0.3.0 | 1K+ | Merged 
17 | 1eceeec | Minesweep| Games | 12.4.2 | 10K+ | Merged 
18 | 7577fb2 | Plees-tracker | Sports | 7.1.5 | 5K+ | Merged 
19 | 7617c90 | Plees-tracker | Sports | 7.1.5 | 5K+ | Merged 
20 | 3fb3725 | Tickmate | Time | 1.4.12 | 5K+ | Merged 
21 | aa705c7 | APK Explorer| System | v0.16 | 1K+ | Merged 
22 | d23ae3b | Democracy| Media | 4.2.0 | 10K+ | Merged 
23 | 33eb95c | SexyTopo | Science | 1.6.0 | 1K+ | Pending 
24 | c87c659 | Carnet | Writing | 0.24.1 | 10K+ | Pending 
25 | 57da1ce | Carnet | Writing | 0.24.1 | 10K+ | Pending 
26 | 757a286 | Easer | System | 0.8.2 | 10K+ | Merged 
27 | a8c9944 | Easer | System | 0.8.2 | 10K+ | Merged 
28 | 3a4e369 | Repeater | Connect | 0.5 | 1K+ | Merged 
29 | 9567661 | Watomatic | Internet | 1.20 | 10K+ | Merged 
30 | 5225479 | ChessClock | Games | 2.5.0 | 10K+ | Merged 
31 | e7a3b34 | Look4Sat | Science | 2.5.3 | 10K+ | Merged 
32 | 838ce80 | Look4Sat | Science | 2.5.3 | 10K+ | Merged 
33 | 8dc6962 | Badreads | Reading | 0.1.6 | 1K+ | Pending 
34 | 703a262 | PDFConverter | Media | 8.8.1 | 100K+ | Merged 
35 | e3f9368 | Calendar | System | 3.2 | 1K+ | Merged 
36 | 8fa1de5 | Calendar | System | 3.2 | 1K+ | Merged 
37 | 35b155f | DotsBoxes | Games | 0.7.5 | 10K+ | Pending 
38 | 1956edc | Monitor| System | 3.3.1 | 1K+ | Merged 
39 | c2fff98 | Léon | System | 0.5.0 | 1K+ | Merged 
40 | e5b359d | Goodtime | Time | 2.2.7 | 500K+ | Merged 
41 | 414735f | RCX | System | 1.12.2 | 5K+ | Merged
42 | b89745d | Classic | System | 3.1.4 | 10K+ | Merged
43 | c64fc26 | PxerStudio| Graphics | 1.2.0 | 1K+ | Merged 
44 | 1812bbe | Gelli | Media | 1.3.2 | 50K+ | Merged 
45 | f1c2fcc | Gelli | Media | 1.3.2 | 50K+ | Merged 
46 | 63fe9f7 | IPCam | Internet | 2.1.0 | 1K+ | Merged 
47 | 9e1a2ab | AF Weather | Internet | 1.3 | 1K+ | Merged 
48 | c93c216 | Track\|Graph | Sport | 1.14.0 | 10K+ | Merged 
49 | 31428c0 | Tunerly | Media | 1.0.5 | 1K+ | Merged 
50 | 7fd8e24 | Headi| Health | 1.10.8 | 1K+ | Merged 
51 | 076f8e8 | Frost| Media | 2.1.2 | 10K+ | Merged 
52 | eb6cfb1 | Frost| Media | 2.1.2 | 10K+ | Merged 
53 | 6daf966 | WeeklyBudget | Money | 1.4 | 1K+ | Merged 
54 | 3f6aff3 | WeeklyBudget | Money | 1.4 | 1K+ | Merged 
55 | d0dfa62 | WeeklyBudget | Money | 1.4 | 1K+ | Merged 
56 | 18eab53 | WeeklyBudget | Money | 1.4 | 1K+ | Merged 
57 | 7561bdc | WeeklyBudget | Money | 1.4 | 1K+ | Merged 
58 | fdbaaa5 | WeeklyBudget | Money | 1.4 | 1K+ | Merged 
59 | d59b701 | HeartBeat | Health | 1.2 | 1K+ | Merged 
60 | 1e34fb9 | HeartBeat | Health | 1.2 | 1K+ | Merged 
61 | 7856db5 | 8Vim Keyboard | System | 0-7 | 1K+ | Merged 
62 | 87d50c8 | Birday | Time | 2.1.0 | 10K+ | Merged 
63 | 8a19e40 | Birday | Time | 2.1.0 | 10k+ | Merged 
64 | eb6cfb1 | Acrtions| Media | 2.0.0 | 10K+ | Merged 
65 | 5a3fb30 | Openboard | System | 1.4.3 | 50K+ | Merged 
66 | c7c9089 | VocableTrainer | Education | 0.7.3 | 1K+ | Merged 
67 | 4c66c93 | WaterTracker | Health | 0.1.3 | 1K+ | Merged 
68 | 20a3b38 | Secure File | Security | 0.1.8 | 2K+ | Pending 
69 | 380f58d | Secure File | Security | 0.1.8 | 2K+ | Pending 
70 | 753391a | Secure File | Security | 0.1.8 | 2K+ | Pending 
71 | 4da2987 | Secure File | Security | 0.1.8 | 2K+ | Pending 
72 | 8767e55 | AppIntro| Plugin | 1.6.0 | 100K+ | Merged 
73 | 48398cf | QDict | Reading | 2.1.3 | 1K+ | Merged
74 | f5e0f65 | QDict | Reading | 2.1.3 | 1K+ | Merged
75 | 3baa4d1 | QDict | Reading | 2.1.3 | 1K+ | Merged
76 | 16f181a | AnotherMonitor | System | 3.1.1 | 10K+ | Merged
77 | ecc8017 | AutoDark | System | 3.0.3 | 1K+ | Merged
78 | ba847f3 | DSAA | System | 1.0 | 1K+ | Merged
79 | d88a0a9 | DSAA | System | 1.0 | 1K+ | Merged
80 | 86e18da | DSAA | System | 1.0 | 1K+ | Merged
81 | 71e198d | DSAA | System | 1.0 | 1K+ | Merged
82 | ee19945 | DMWallpaper | Theming | 1.1.2 | 1K+ | Merged
83 | e93d6a4 | RemoteNumpad | System | 1.7.1 | 1K+ | Pending
84 | 566f092 | Baby Dots | Media | 1.5.0 | 1K+ | Merged
85 | 2cdbba6 | BlockPuzzle | Game | 7.0 | 1K+ | Merged
86 | d1fcda4 | OpenHub | Internet | 3.2.1 | 100K+ | Pending
87 | eeb9604 | Planisphere | Education | 1.8.0 | 1K+ | Pending
88 | 5e10505 | osmfocus | Navigation | 1.1.1 | 1K+ | Pending
89 | c35d38f | InfiniList | Writing | 1.0.5 | 1K+ | Merged
90 | ae898bb | bitcoin | Finance | 8.1.0 | 10K+ | Pending
91 | 12a05cf | slimlauncher | System | 2.4.2 | 100K+ | Pending
92 | e707b9f | Forecastie | Internet | 1.17.3 | 10K+ | Merged
93 | c837a7b | Forecastie | Internet | 1.17.3 | 10K+ | Merged
94 | 3d578d2 | UML Class | Develop | 1.0 | 1K+ | Merged
95 | f6d1f67 | cetoolbox | Education | 1.4.5 | 1K+ | Pending
96 | b22cf85 | URLSanitizer | Internet | 1.4.0 | 1K+ | Merged
97 | 46bdc8f | WalletCount | Money | 1.1 | 1K+ | Pending
98 | 374caff | WalletCount | Money | 1.1 | 1K+ | Pending
99 | f4c1744 | WalletCount | Money | 1.1 | 1K+ | Pending
100 | 471afe6 | WalletCount | Money | 1.1 | 1K+ | Pending
101 | 630964f | WalletCount | Money | 1.1 | 1K+ | Pending
102 | eb6332c | WalletCount | Money | 1.1 | 1K+ | Pending
103 | 8ee9d4f | NotifiCron | Time | 1.4.2 | 1K+ | Merged
104 | 66c9c05 | J2MELoader | Game | 1.7.0 | 1M+ | Merged
105 | c376e97 | Dawn | Internet | 0.12.2 | 5K+ | Merged
106 | 1cc0ecb | YLW | Internet | 5.7.3 | 5K+ | Pending
107 | 644d388 | MHWD | Games | 2.1.1 | 100K+ | Pending
108 | ec03adc | MHWD | Games | 2.1.1 | 100K+ | Pending
109 | 195b5ed | openfood | Health | 3.6.8 | 1M+ | Pending
110 | cc770b9 | openfood | Health | 3.6.8 | 1M+ | Pending
111 | 9800ae7 | openfood | Health | 3.6.8 | 1M+ | Pending
112 | f8e993e | openfood | Health | 3.6.8 | 1M+ | Pending
113 | 8b20f74 | openfood | Health | 3.6.8 | 1M+ | Pending
114 | a51b1ac | openfood | Health | 3.6.8 | 1M+ | Pending
115 | b34555e | Anuto TD | Games | 0.7 | 10K+ | Pending
116 | 467857f | Anuto TD | Games | 0.7 | 10K+ | Pending
117 | 1249656 | OSMTracker | Navigation | 1.0.1 | 10K+ | Pending
118 | 8443ed2 | altlauncher | Navigation | 1.0.1 | 10K+ | Pending
119 | 846rfd1 | altlauncher | Navigation | 1.0.1 | 10K+ | Pending
120 | 6r43dd5 | altlauncher | Navigation | 1.0.1 | 10K+ | Pending
121 | 4343bd2 | altlauncher | Navigation | 1.0.1 | 10K+ | Pending

UIBat can repair 121 unique UI display issues from GitHub. We submit 121 pull requests to the develop in GitHub, **86 of them are successfully merged** by developers, while the remaining are still pending (**none of them is rejected**). Actually, the user study also suggests the relatively high degree of satisfaction of our proposed fixing, i.e., **92 merged pull requests** and **66** of them receiving **“like”** in Github. 

When merging pull requests, the developers express thanks such as "*Thank you very much for this improvement, this is great. Much appreciated!*" (i.e., 4345457, PicardScanner), "*Very nice! Thank you for this contribution!*" (i.e., 8a76280, AlarmClock).
Furthermore, developers also express their thought about UI display issues "*I have to admit I didn't think of this kind of issue at first and after a bit of testing the problem seems to be a bit more complex beside these login screens.*" (i.e., 5fcf8e1, OpenWebWeaver).

For the idea of ''Search and Destroy'' of our UIBat, the developers of GPSlogger (a project with 1.4K stars and 1 million downloads on GitHub) give us an approving look with the message shown in below figure.

![pull request](https://github.com/UIBat/UIBat/blob/main/pull%20request.png) 
