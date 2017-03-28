# {{ page.title }}

Release tag: {{ page.release_tag }}

Builds repository commit ID: {{ page.builds_commit }}

Versions repository commit ID: {{ page.versions_commit }}

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
            <td> <a href="{{ package.clone_url}}">{{ package.name }}</a> </td>
            <td> {{ package.version }} </td>
            <td> {{ package.release }} </td>
            <td> {{ package.branch }} </td>
            <td> {{ package.commit_id }} </td>
        </tr>
        {% endfor %}
    </tbody>
</table>
