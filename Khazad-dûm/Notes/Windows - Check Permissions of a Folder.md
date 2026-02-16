10-14-2025 13:52

Tags: [[Windows]] [[System Administration]]

To check the permissions of a folder in Windows, you can use several command-line tools and methods. The most common and effective approach is using PowerShell with the `Get-Acl` cmdlet, which retrieves the security descriptor of the folder, including its owner and access control lists (ACLs). For example, to view the permissions of a folder, run:

```
Get-Acl "C:\Path\To\Folder"
```

This command displays the folder path, owner, and access list. To see more detailed information, such as specific file system rights, inheritance flags, and access control types, use the `Access` property:

```
(Get-Acl "C:\Path\To\Folder").Access
```

This provides a comprehensive view of the permissions assigned to users and groups, including whether they are inherited from a parent folder via the `IsInherited` property.

For a more user-friendly output, you can format the results in a table using `ft -AutoSize`:

```
Get-Acl "C:\Path\To\Folder" | Select-Object -ExpandProperty Access | Format-Table -AutoSize
```

If you want to filter permissions for a specific user or group, such as "Administrators" or "SYSTEM", use the `Where-Object` cmdlet:

```
Get-Acl "C:\Path\To\Folder" | Select-Object -ExpandProperty Access | Where-Object {$_.IdentityReference -like "*Administrators*"} | Format-Table -AutoSize
```
## References


