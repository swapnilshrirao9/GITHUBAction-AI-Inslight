GitHub Repo https://github.com/swapnilshrirao9/GITHUBAction-AI-Inslight
Create Ollama-API Always update the Vscode port forword option
# open vscode and open terminal > port> add port value 11434 make Visblity Public

Step A: Add the Tunnel URL to GitHub Secrets
 Go to your GITHUBAction-AI-Inslight repository ---> Settings ---> Secrets and variables --->Actions.
 Add a new secret named OLLAMA_BASE_URL and paste your VS Code forwarded URL (without a trailing slash).
 Create Secret OLLAMA_GITHUB_TOKEN in the  repository ---> Settings ---> Secrets and variables 

Step B Change the line 
https://swapnilshrirao9.github.io/AI-GithubAction/



Invoke-RestMethod -Uri "https://<<<URL of VSCode>>>/v1/chat/completions" -Method Post -ContentType "application/json" -Body '{"model":"mistral","messages":[{"role":"user","content":"Hi"}]}'