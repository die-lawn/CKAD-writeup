# Hello fellow peeps! Welcome to the Certified Kubernetes Application Developer (CKAD) Zero to Hero Guide!
This guide is tailored to those who want to pass their CKAD cert and who are new to K8s. There are no prerequisites for this certification but there are some things you must be familiar with prior to starting the course to make things much easier like VIM, basic linux, command line. Using this info will help you pass the CKAD exam. <br/>

 1. **Understand the basics of VIM (Text editor)**
      - There are other options for a text editor but as you follow along in CKAD courses, you'll see that VIM is the preferred text editor.
       	- How to list files at your current path: ls ![image](https://user-images.githubusercontent.com/105947650/169603624-37031be0-009b-4f00-827c-50df166dbb58.png)

       
			 
		 - View your current path: pwd  <br/> ![image](https://user-images.githubusercontent.com/105947650/169603653-3d6b8185-4fd0-46d0-9ec5-f0e1527e839f.png)
		 - Go to another path: cd *then path here* ![image](https://user-images.githubusercontent.com/105947650/169603684-64a10e1f-ea73-4679-99d6-2dd6f46db01b.png)
		 - Go to the path above current path: cd .. ![image](https://user-images.githubusercontent.com/105947650/169603824-66fb08e0-8f97-489b-9a24-bea693d160e9.png)
		 - Go to home directory: cd ~ 
		 - Create and open a yaml file called testpod.yaml at the current path: vi testpod.yaml ![image](https://user-images.githubusercontent.com/105947650/169603878-396ddafb-6c5c-4a5d-be1f-585e2265b532.png)
		 - Type in your newly created test file: i (insert should appear at the bottom of the file -- then press esc to stop) ![image](https://user-images.githubusercontent.com/105947650/169604017-f1b72225-1c02-4120-a063-0cf8fff04722.png)
		 - Save changes and exit VIM editor: esc --> :wq ![image](https://user-images.githubusercontent.com/105947650/169604062-115a4d1f-ccd2-4f69-b797-15ca3166d51d.png)
		 - Don't save changes: esc --> :q! ![image](https://user-images.githubusercontent.com/105947650/169604127-33d8219e-ee21-4454-bec5-a2c56065f0a5.png)
		 - Remove/delete file: rm filename ![image](https://user-images.githubusercontent.com/105947650/169604176-83c60bc6-4a29-4b9b-b2a6-01100b196197.png)
 2. **Once you understand VIM, you should begin this Udemy Course** [Kubernetes Certified Application Developer (CKAD) with Tests](https://www.udemy.com/course/certified-kubernetes-application-developer/)
     - This course has everything you need to cover the exam objectives. There are labs at the end of each lesson.  In order to fully grasp content, practice the labs enough to be able to solve them without help from the solution videos
     - There is a GAME of PODS game in the course. I skipped that because it still references an older version of Kubernetes
     - Once you finish the course, apply the same technique to the lightning labs/Mock exams
     - After you master those, open your killer.sh sessions. You are granted two with an exam purchase and they are extremly similar to the exam
 3. **[Killer.sh](killer.sh)**
    - This simulator is the best prep for the exam
    - With K8 exams, you are allowed to use official documentation. Linked here is a compilation of bookmarks to make navigating easier [bookmarks for chrome](https://github.com/reetasingh/CKAD-Bookmarks/blob/master/kubernetes.io.html)
    - Use killer SH as if it were the real exam.  Take the test and use the official documentation.  If you are stuck on a question, study the section, reference the answers and be able to solve AND understand the steps until you can solve it 100%
    - I paid for about 4 sessions on top of what was provided with the exam voucher and it's what helped me bring my score to a 51% to an 88%
    - Once you are scoring more than 100 points on the killer sh sessions, book your exam
 4. **Kode Kloud Slack** 
    - There is a slack channel dedicated to CKAD,CKS,CKS which is linked in the Udemy course. Join that group and view the pinned messages. Members in there speak about the experience with the exams and provide many tips in order to pass the exam
 5. **Tips for the exam** 
    - There are 16 practical lab questions for the CKAD exam and you have 120 minutes to complete the exam. Using alias' and autocomplete within the exam environment is essential for success. The commands are in the [official documentation ](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)so there isn't a need to memorize anything. At the start of each K8 lab/exam you attempt, run the follow commands at a minimum:  
      - alias k=kubectl
      - complete -F __start_kubectl k 
      - export do="--dry-run=client -o yaml"
    - Having these alias' set, shaves time of each command you type out.
      - kubectl -n default run testpod --image=nginx --dry-run=client -o yaml > testpod.yaml <br/>
        ~~~~is the same command as~~~~ <br/>
        k -n default run testpod --image=nginx $do > testpod.yaml
    - Use the help & explain command to grab more information regarding resource types 
       ![image](https://user-images.githubusercontent.com/105947650/169630519-07ff7745-0c3c-4338-9c02-978468d39ea6.png) 
       ![image](https://user-images.githubusercontent.com/105947650/169630575-f02df14a-ba4c-4c2d-982b-e5c40ca682e6.png)
       ![image](https://user-images.githubusercontent.com/105947650/169630701-714a2308-94f3-483c-8ab6-98ad1f5dfe60.png)
    - Always use imperative commands when you can vs any other method(ex: editing an image of a deployment, resource requests, creating a pod with args)
      - [This Kubectl Command documentation page is gold when it comes to imperative commands.](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands) 
        ![image](https://user-images.githubusercontent.com/105947650/169630896-30e38a3b-bd2f-4c1d-8837-729a7a8b324e.png)
	The command aboves changes the service account used on a specific deployment in one command. There are many methods to solve K8 questions that are similar but for the exams sake, doing the most efficient commands gives you more time to review your answers





     
	
     
 
 6. **MISC resources**
[github exercises](https://github.com/dgkanatsios/CKAD-exercises) --
[CKAD blog](https://mengying-li.medium.com/failed-ckad-first-attempt-my-journey-to-improve-exam-score-from-53-to-98-in-a-month-part-1-badde0746231)--
[katacode labs](https://www.katacoda.com/liptanbiswas/courses/ckad-practice-challenges)--



**TLDR:**  <br/>![image](https://user-images.githubusercontent.com/105947650/169604247-477598e4-b215-4440-baa1-abf574aec475.png)

