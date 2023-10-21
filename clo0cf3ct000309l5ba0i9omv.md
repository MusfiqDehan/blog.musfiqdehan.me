---
title: "Suppose, you have two git branches dev and main. You want to delete main branch and convert the dev branch into main branch. How can you do that?"
seoDescription: "Recently, I have faced an interesting problem. For a project, I had to delete my main branch and convert the dev branch into the main branch."
datePublished: Sat Oct 21 2023 17:58:01 GMT+0000 (Coordinated Universal Time)
cuid: clo0cf3ct000309l5ba0i9omv
slug: suppose-you-have-two-git-branches-dev-and-main-you-want-to-delete-main-branch-and-convert-the-dev-branch-into-main-branch-how-can-you-do-that
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1697910091239/8fdd80be-a7a1-495b-828b-de95d6e7452c.png
tags: github, git, branch

---

Recently, I have faced an interesting problem. For a project, I had to delete my `main` branch and convert the `dev` branch into the `main` branch. Though it is possible, I have to be very careful because any mistake can destroy my whole project. Let's discuss, how I did it!

To delete the `main` branch and rename the `dev` branch to `main` in Git, you can follow these steps:

**Please be careful when performing these operations, especially if you're working on a shared repository.**

1. **Ensure you are on the** `dev` **branch:** If you are not on the `dev` branch, switch to it using the following command:
    
    ```bash
    git checkout dev
    ```
    
2. **Merge the changes from** `main` **into** `dev` **(if necessary):** It's a good practice to merge the latest changes from the `main` branch into the `dev` branch to ensure you don't lose any important updates. If there are no changes in `main` that need to be merged, you can skip this step.
    
    ```bash
    git merge main
    ```
    
3. **Delete the** `main` **branch:** To delete the `main` branch, use the following command:
    
    ```bash
    git branch -d main
    ```
    
    If you get an error saying that the branch is not fully merged, use the following command to forcefully delete it:
    
    ```bash
    git branch -D main
    ```
    
4. **Rename the** `dev` **branch to** `main`**:** To rename the `dev` branch to `main`, use the following command:
    
    ```bash
    git branch -m dev main
    ```
    
5. **Push the changes to the remote repository:** After you've made these changes, you should push them to your remote repository so that others can see and use the updated branch names.
    
    ```bash
    git push origin main
    ```
    
    This will push your newly renamed `main` branch to the remote repository and delete the old `main` branch.
    

Now, you've successfully deleted the `main` branch and converted the `dev` branch into the new `main` branch. Make sure to communicate these changes to your team if you're working in a collaborative environment, as it will affect the branch names that others are working with.

Hope you find this article helpful. If you have any suggestions, please write them in the comment section. Thanks.