# Resolving Conflicts in Git

## What Are Conflicts?
Conflicts occur when Git cannot automatically merge changes between branches. This typically happens when changes are made to the same lines of code in different branches.

## Steps to Resolve Conflicts

### 1. Identify Conflicts
When you attempt to merge branches or pull changes from a remote repository, Git will notify you of conflicts. The output will indicate which files have conflicts.

### Example
```sh
Auto-merging file.txt
CONFLICT (content): Merge conflict in file.txt
Automatic merge failed; fix conflicts and then commit the result.
```

### 2. Open Conflicted Files
Open the files with conflicts in your text editor or IDE. Conflicted areas are marked with special conflict markers:

```plaintext
<<<<<<< HEAD
Your changes
=======
Changes from the branch you are merging
>>>>>>> branch-name
```

### 3. Resolve Conflicts
Edit the conflicted files to resolve conflicts. You need to decide how to combine the changes. Remove the conflict markers (`<<<<<<<`, `=======`, and `>>>>>>>`) and make the necessary edits.

### Example
If `file.txt` contains the following conflict:

```plaintext
<<<<<<< HEAD
Your changes
=======
Changes from the branch you are merging
>>>>>>> branch-name
```

You should edit it to resolve the conflict:

```plaintext
Combined changes or the correct version you want to keep
```

### 4. Stage Resolved Files
After resolving conflicts in all files, stage the resolved files using `git add`:

```sh
git add file.txt
```

### 5. Commit the Merge
Finally, commit the resolved merge:

```sh
git commit -m "Resolved merge conflicts"
```

## Additional Tips for Resolving Conflicts

### Use a Merge Tool
Git allows you to use merge tools to help resolve conflicts. You can configure and use a tool like `meld`, `kdiff3`, or others.

#### Configure a Merge Tool
```sh
git config --global merge.tool meld
git config --global mergetool.prompt false
```

#### Use the Merge Tool
```sh
git mergetool
```

### Review Conflicts with `git status`
Use `git status` to see a summary of the conflicted files and ensure you have resolved all conflicts.

```sh
git status
```

### Abort a Merge
If you need to abort the merge process and return to the state before the merge started:

```sh
git merge --abort
```

## Example Workflow

### Step-by-Step Example
1. **Create a Conflict**: Suppose you have two branches, `main` and `feature`.

    ```sh
    # Create and switch to feature branch
    git checkout -b feature

    # Make changes in the feature branch
    echo "Feature change" >> file.txt
    git add file.txt
    git commit -m "Feature changes"

    # Switch back to main branch
    git checkout main

    # Make conflicting changes in the main branch
    echo "Main change" >> file.txt
    git add file.txt
    git commit -m "Main changes"
    ```

2. **Merge and Resolve Conflict**:

    ```sh
    # Attempt to merge feature branch into main
    git merge feature
    ```

    You will see a conflict message. Open `file.txt`:

    ```plaintext
    <<<<<<< HEAD
    Main change
    =======
    Feature change
    >>>>>>> feature
    ```

3. **Resolve the Conflict**: Edit `file.txt` to resolve the conflict:

    ```plaintext
    Main change
    Feature change
    ```

4. **Stage and Commit**:

    ```sh
    git add file.txt
    git commit -m "Resolved merge conflict in file.txt"
    ```

---
