NVM does not support fish shell.

But, We can install the bass plugin to use utilities written for Bash.

Install bass using oh-my-fish.
```

omf install bass
```

Install nvm
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash
```


Add fish function to ~/.config/fish/functions/nvm.fish to load nvm:
``` 
sudo touch ~/.config/fish/functions/nvm.fish
```
Copy the code below to nvm.fish file.
```
function nvm
    bass source ~/.nvm/nvm.sh --no-use ';' nvm $argv
end
```

NVM is ready to use. Check with 

nvm --version
