# My useful list of Alias
Some useful git aliases I may need in the future if I change my computer.

**Add this to .gitconfig file**

[alias]
	st = status
	rm-all = "!f(){\
			git branch | grep -v "feature/21.1.0" | grep -v ^* | xargs git branch -d;\
	}; f"
	rm-all-force = "!f(){\
			git branch | grep -v "feature/21.1.0" | grep -v ^* | xargs git branch -D;\
}; f"
	ignore = update-index --assume-unchanged
	unignore = update-index --no-assume-unchanged
	ignored = !git ls-files -v | grep "^[[:lower:]]"
