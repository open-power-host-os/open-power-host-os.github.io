# {{ page.title }}

Release tag: {{ page.release_tag }}

Builds repository commit ID: {{ page.builds_commit }}

Versions repository commit ID: {{ page.versions_commit }}

{{ page.content }}

# Components

<style type="text/css">
.main-item{background-color:#CCCCCC;border-style:solid;border-width:0px;border-top-width:1px;border-bottom-width:1px;}
.secondary-item{border-style:solid;border-width:0px;border-top-width:0px;border-bottom-width:0px;white-space:nowrap;}
tr:hover{background-color:#DDDDDD}
</style>

<table>
    <thead>
        <tr>
            <th>Repository</th>
            <th>Branch</th>
            <th>Commit ID</th>
        </tr>
    </thead>
    <tbody>
        {% for package in page.packages %}
        <tr>
            <td class="main-item" colspan="3"> {{ package.name }}-{{ package.version }}-{{ package.release }} </td>
        </tr>
        {% for source in package.sources %}
        {% assign project_url = source.src | replace: 'svn://', 'http://' %}
        {% assign project_name = source.src | split: '/' | last | replace: '.git', '' %}
        <tr>
            <td class="secondary-item"> <a href="{{ project_url }}">{{ project_name }}</a> </td>
            <td class="secondary-item"> {{ source.branch }} </td>
            <td class="secondary-item"> {{ source.commit_id }} </td>
        </tr>
        {% endfor %}
        {% endfor %}
    </tbody>
</table>
