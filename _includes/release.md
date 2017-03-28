# {{ page.title }}

Release tag: {{ page.release_tag }}

Builds repository commit ID: {{ page.builds_commit }}

Versions repository commit ID: {{ page.versions_commit }}

{{ page.content }}

# Components

<style type="text/css">
.main-item{border-style:solid;border-width:0px;border-top-width:1px;border-bottom-width:1px;}
</style>
<table>
    <thead>
        <tr>
            <th>Package name</th>
            <th>Version</th>
            <th>Release</th>
            <th>Branch</th>
            <th>Commit ID</th>
        </tr>
    </thead>
    <tbody>
        {% for package in page.packages %}
        <tr>
            <td class="main-item"> <a href="{{ package.clone_url}}">{{ package.name }}</a> </td>
            <td class="main-item"> {{ package.version }} </td>
            <td class="main-item"> {{ package.release }} </td>
            <td class="main-item"> {{ package.branch }} </td>
            <td class="main-item"> {{ package.commit_id }} </td>
        </tr>
        {% endfor %}
    </tbody>
</table>
