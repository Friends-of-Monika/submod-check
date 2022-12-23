# 🔧 Submod Check

A [reusable workflow][1] that you can use to pre-emptively perform submod syntax
and `init` block tests on every push.

## 📗 Example usage

1. Create a file called `check.yml` (any name works, it only serves as a note
   for you and other users to distinguish workflows) in a directory
   `.github/workflows`. Populate it with the following content:

   ```yml
   name: Run checks

   on: push

   jobs:
     check:
       uses: friends-of-monika/submod-check/.github/workflows/check.yml@master
       with:
         paths: |-
           PATH_TO_YOUR_SUBMOD_DIRECTORY
   ```

2. Replace `PATH_TO_YOUR_SUBMOD_DIRECTORY` with a path (relative to repository
   root) to the directory where your submod's .rpy files are located. For example,
   imagine you have a directory called `mod` in your repository where all script
   files reside, in this case, you'd set `paths` value to the following:

   ```yml
   paths: |-
     mod
   ```

3. Commit and push the changes.


[1]: https://docs.github.com/en/actions/using-workflows/reusing-workflows#reusable-workflows-and-starter-workflows