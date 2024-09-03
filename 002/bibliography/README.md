# Teaching RSE: bibliography database

We use a single, shared BibTeX bibliography file for all papers in the teaching RSE project. This is imported as a Git submodule from this repository. If you want to contribute new entries to the bibliography, you need to add them there.

After adding the entries here, update the submodules in your branch of the respective repository that uses this submodule:

```shell
git submodule update --remote --merge
git add bibliography
git commit -m "Update bibliography submodule"
git push
```

In your pull request, you should see `bibliography` as a one-line modification, with the comment `Submodule bibliography added at <commit hash>`. Make sure that this commit hash points to the state of the bibliography repository you want to. This means that it should not point to a commit in your fork not on the main repository. Be careful also to not point to a commit that you later squash.
