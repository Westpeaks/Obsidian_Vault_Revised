2025-02-11 09:27

Tags: [[Terraform]] [[Cloud]] [[DevOps]] [[Cheat Sheet]]

# Terraform Command Cheat Sheet

![[terraform-cheatsheet-scaled.jpg]]

## Top 10 most useful Terraform commands

You can also enter the terraform command and then a subcommand with `-h` or `--help` to pull up a list of commands that are specific to that subcommand. Let's do a walkthrough of the 10 Terraform commands you may end up using the most.

**1. `fmt`**  
When I’ve finished my Terraform configuration, I want to make sure that everything is formatted correctly, so I run the `fmt` command first. This command reformats your configuration in the standard style, so it’ll make sure that the spacing and everything else is formatted correctly. If it comes back blank, that means the configuration files within your working directory are already correctly formatted. If it does format a file, it will let you know what file it touched.

**2. `init`**  
After you use the `format` command, you’ll want to initialize your working directory to prepare it for what you need. The `init` command looks at your configuration files and determines which providers and modules it needs to pull down from the registry to allow your configuration to work properly.

**3. `validate`**  
Once you’ve initialized the directory, it’s good to run the`validate` command before you run `plan` or `apply`. Validation will catch syntax errors, version errors, and other issues. One thing to note here is that you can’t run `validate` before you run the `init` command. You have to initialize the working directory before you can run the validation.

**4. `plan`**  
Next, it’s always a good idea to do a dry run of your plan to see what it’s actually going to do. You can even use one of the subcommands with `terraform plan` to output your plan to apply it later.

**5. `apply`**  
And then of course you have your `apply` command, which is one of the commands you’re going to use the most. This is the command that deploys or applies your configuration to a provider.

**6. `destroy`**  
The `destroy` command, obviously, will destroy your infrastructure — or, when used with the `target` flag, individual resources within your infrastructure.

**7. `output`**  
If you’ve put together a good output variable file, you can use the `output` command to make those defined outputs to display certain information. For example, if you’re deploying EC2 instances, you can output tag names, instance names, instance IDs, the IP of the instance, and so on. You can gather some really good information that makes it simple to look up later. And if you’re working as a team, people coming behind you can use the `output` command to figure things out and get up to speed.

**8. `show`**  
The `show` command shows the current state of a saved plan, providing good information about the infrastructure you’ve deployed. For example, if you have an EC2 instance or a VM deployed in your configuration, it’ll show you the state that it’s in — if it’s up and ready or if it’s being terminated. It also provides useful information like IP addresses.

**9. `state`**  
Another good way to check your work is to use the `state` command. If you use `state` and then the subcommand `list`, it’ll give you a consolidated list of the resources that are being managed by your configuration. If you are moving your Terraform instance, such as from a local instance to a remote backup, you would use the `state mv` command. And just like the `show` command, there’s a `state show` command that shows a resource in the state. You can also remove instances from a state by using the `state rm` command.

**10. `version`**  
You’ll use the `version` command quite a bit to check your Terraform version, especially if you have any version conflicts. Sometimes providers work only with certain versions of Terraform, so if you’re defining those versions within your configuration, you’ll need to use the `version` command here and there.  

Those are some of the most popular Terraform commands. Keep in mind that `-h` is a very handy way to quickly look up commands when you’re not 100% sure how to use one or what it does, especially when you’re getting started. Take a look at it when you get a chance!
## References

[Ultimate Terraform Commands Cheat Sheet](https://www.pluralsight.com/resources/blog/cloud/the-ultimate-terraform-cheatsheet)

