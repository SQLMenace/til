To make a parameter mandatory, use ValidateNotNull().


```Powershell
	param(
		[ValidateNotNull()]$Folder = $(throw "ScriptFolder is mandatory, please provide a value.")

	)
	cd $Folder
	(dir $Folder) | ForEach-Object { 
		$name = $_.name
		Write-Host "*****${name}"
	}
	```
