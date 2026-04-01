<frontmatter>
  title: Desktop App Guide
  layout: default.md
  pageNav: 4
  pageNavTitle: "Topics"
</frontmatter>

<br>

<br>

# Installation Instructions
## Windows
1. Download the .exe file from the [Git Visor Desktop App](https://github.com/git-visor/desktop-app/releases/latest)
2. Run the .exe file
<box type="warning">
If you encounter a warning about the app being from an untrusted developer, click "More info" and then "Run anyway" to proceed with the installation.
</box>
3. Wait for the installation to complete, and the app will launch automatically.

<br><br>

## macOS
1. Download the .dmg file from the [Git Visor Desktop App](https://github.com/git-visor/desktop-app/releases/latest)
2. Open the .dmg file and drag the Git Visor app to your Applications folder
3. Launch the app from your Applications folder
<box type="warning">
If you encounter a warning about the app being from an untrusted developer, click the question mark icon on the top right and follow the instructions to open the app anyway.
</box>

# How to Use
1. Open Git Visor and select "Open Repository" to choose a Git repository on your local machine. Make sure to select the folder that contains the .git directory of your repository. Your screen should now look something like this:
<img src="{{baseUrl}}/images/desktop-repository.png" alt="Open Repository" class="img-fluid my-3" width="600" height="400">
2. Once the repository is loaded, head over to the "Objects" tab to view the internal state of your Git repository. There are two choices of visualisation: "List" and "Graph". The "List" view shows a list of all Git objects in the repository, while the "Graph" view shows a visual representation of the commit history and branch structure of the repository.
<img src="{{baseUrl}}/images/desktop-point-at-objects-tab.png" alt="Objects Tab" class="img-fluid my-3" width="600" height="400">
<img src="{{baseUrl}}/images/desktop-list-view.png" alt="List View" class="img-fluid my-3" width="600" height="400">
<img src="{{baseUrl}}/images/desktop-graph-view.png" alt="Graph View" class="img-fluid my-3" width="600" height="400">
3. In both views, you can click on any object to view its details, such as its type, size, and content. In the "Graph" view, you can also drag nodes around to rearrange the graph for better visibility.
4. On the left sidebar, the branch panel allows you to select which branches to display in the graph.
<img src="{{baseUrl}}/images/desktop-branch-panel.png" alt="Branch Panel" class="img-fluid my-3" width="600" height="400">
5. <a id="export-json"></a>[Optional] In the repository tab, you can also export JSON data of the Git objects in the repository by clicking on the "Export JSON" button. You can then upload it to your github and use the link to [load the data in the web app]({{baseUrl}}/contents/guide-web.html#load-url) if you want to view the visualisation on the web app or share it with others.
<img src="{{baseUrl}}/images/desktop-export-json.png" alt="Export JSON" class="img-fluid my-3" width="600" height="400">

# Navigating the Graph
To understand more about what the graph represents and how to navigate it, check out the [Graph Navigation Guide]({{baseUrl}}/contents/graph-navigation.html).

