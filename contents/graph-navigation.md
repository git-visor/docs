<frontmatter>
  title: Graph Navigation
  layout: default.md
  pageNav: 4
  pageNavTitle: "Topics"
</frontmatter>

<br>

<br>

# Graph Navigation Guide
## Git Objects
In Git, there are three main types of objects: commits, trees, and blobs. Each object will have a unique hash that identifies it. The graph visualisation in the web app represents these objects and their relationships.

## Graph Layout
The graph is laid out in a way that shows the relationships between the objects. However, you can drag the nodes around to rearrange the graph for better visibility. You can also pan around the graph by clicking and dragging on the background.

The lines connecting the nodes represent the relationships between the objects. For example, a commit node will have lines connecting it to its parent commit(s) and its root tree. A tree node will have lines connecting it to the blobs and subtrees it contains.

## Object Details
When you click on a node in the graph, you can view its details in the side panel. The details will show the object's type, hash, and other relevant information. The information displayed depends on the type of object you are viewing.
### <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" color='#60a5fa'> <path d="M12 12m-3 0a3 3 0 1 0 6 0a3 3 0 1 0 -6 0 M12 3v6 M12 15v6"></path> </svg> Commits 

Commits represent a snapshot of the repository at a specific point in time. They contain metadata such as the **author**, **date**, and **commit message**. Each commit will point to a **root tree** (unique unless the commit is a merge commit) and may have **parent commit(s)**. The commit details also show the changes made to each file. To know more about how to read them, refer to [this guide](https://stackoverflow.com/questions/38159304/how-to-read-git-show-command-output).
<box type="info">
In the actual Git repository, the file changes are not stored as part of the commit object. Instead, they are derived from the differences between the tree objects that the commit points to. The web app uses the <code>git show</code> command to compute these differences and display them in the commit details.
</box>

<img src="{{baseUrl}}/images/graph-commit-detail.png" alt="Commit Object" width="500" height="450">
<br>
<br>

### <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" color='#4ade80'> <path d="M4 20h16a2 2 0 0 0 2-2V8a2 2 0 0 0-2-2h-7.93a2 2 0 0 1-1.66-.9l-.82-1.2A2 2 0 0 0 7.93 2H4a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2Z"></path> </svg> Trees

Trees can be thought of as directories in the file system. They contain references to [blobs](#blobs) (files) and other [trees](#trees) (subdirectories). The tree objects show the file names, their types (blob or tree), and their corresponding hashes.
<box type="info">
Although the folder name is shown in the tree details, it is not actually stored in the tree object. The tree object only contains the file name, type, and hash of each entry. The folder name is shown in the web app for better readability, but it is not part of the actual Git object structure.
</box>
<img src="{{baseUrl}}/images/graph-tree-detail.png" alt="Tree Object" width="500" height="450">
<br>
<br>

### <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" color='#facc15'> <path d="M14.5 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V7.5L14.5 2z M14 2v6h6 M16 13H8 M16 17H8 M10 9H8"></path> </svg> Blobs

Blobs represent the contents of files. They do not contain any metadata about the file, such as its name or permissions. Instead, they only store the file's content and its hash. This means that if two files have the same content, they will have the same blob hash, even if they have different names or are located in different directories. This is how a Git repository can efficiently store multiple versions of the same file without duplicating the content.

<box type="info">
Just like trees, the file name is not stored in the blob object. The blob only contains the file content and its hash. The file name is shown in the web app for better readability, but it is not part of the actual Git object structure.
</box>

<img src="{{baseUrl}}/images/graph-blob-detail.png" alt="Blob Object" width="500" height="450">
<br>
<br>