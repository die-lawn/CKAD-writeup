# Hello fellow peeps! Welcome to the Certified Kubernetes Application Developer (CKAD) Zero to Hero Guide!
This guide is tailored to those who want to pass their CKAD cert and who are new to K8s. There are no prerequisites for this certification but there are some things you must be familiar with prior to starting the course to make things much easier like VIM, basic linux, command line. Using this info will help you pass the CKAD exam. <br/>

 **Introduction/About Me**
 - I recently joined my company as a Junior SRE and understanding Kubernetes was apart of our onboarding documents.  After some exploring, I thought to myself "Why not go for my CKAD?".  Which is what I did!  Having an understanding of K8s and grabbing the cert would only add value to my team and I due to a push for container orchestration within the organization and the SRE/DevOps space as a whole. My background prior to this was a few years in military healthcare and 1 year of Java development which shows there isn't a need to be very technical proficient to pursue the CKAD. You only have to be ready to practice and not give up :) I ended up passing the exam on my 3rd attempt so use this tips to pass on your first attempt!

 1. **Understand the basics of VIM (Text editor)**
      - There are other options for a text editor but as you follow along in CKAD courses, you'll see that VIM is the preferred text editor.
       	 - [This is a VIM editor cheatsheet](https://vim.rtorr.com/)
       	 - Some example commands/vim commands you should be comfortable with:
       	 	- ``` vi testpod.yaml``` creating a yaml file named testpod
       	 	- ``` :wq``` save & quit inside the editor
       	 	- ```:q!``` quit and throw away unsaved changes
       	 	- ``` cp testpod.yaml pod.yaml ``` copy contents of testpod.yaml to pod.yaml
       	 	- ``` grep -i A30``` [grep'n](https://ryanstutorials.net/linuxtutorial/cheatsheetgrep.php)
       
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
      - ```alias k=kubectl```
      - ```complete -F __start_kubectl k``` 
      - ```export do="--dry-run=client -o yaml"```
    - Having these alias' set, shaves time of each command you type out.
      - ```kubectl -n default run testpod --image=nginx --dry-run=client -o yaml > testpod.yaml``` <br/>
        equals
      - ```k -n default run testpod --image=nginx $do > testpod.yaml```
    - Use the help & explain command to grab more information regarding resource types 
       - ``` kubectl get pods --help```
       - ``` kubectl explain cronjob.spec```
    - Always use imperative commands when you can vs any other method(ex: editing an image of a deployment, resource requests, creating a pod with args)
      - [This Kubectl Command documentation page is gold when it comes to imperative commands.](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands) 
      - EX: ```kubectl set serviceaccount deployment nginx-deployment serviceaccount1```
      - The command aboves changes the service account used on a specific deployment in one command. There are many methods to solve K8 questions that are similar but for the exams sake, doing the most efficient commands gives you more time to review your answers





     
	
     
 
 6. **MISC resources**
[github exercises](https://github.com/dgkanatsios/CKAD-exercises) --
[CKAD blog](https://mengying-li.medium.com/failed-ckad-first-attempt-my-journey-to-improve-exam-score-from-53-to-98-in-a-month-part-1-badde0746231)--
[katacode labs](https://www.katacoda.com/liptanbiswas/courses/ckad-practice-challenges)--

**Conclusion**
- The CKAD is a structured way of learning which also provides a lot of hands-on/practical labs that will have a direct impact on K8 use in your organization/team.  You will need to practice quite a bit but do not be afraid of failing.  Each mock exam brings you closer to passing the exam and reinforces knowledge.  Passing the exam was not only an accomplishment but allowed me to directly contribue to the team since I felt comfortable configuring applciations right after I got my cert. If you're already using K8s and are ready for a challenge.... go fo it! :)




**TLDR:**  <br/>![image](https://user-images.githubusercontent.com/105947650/169604247-477598e4-b215-4440-baa1-abf574aec475.png)

