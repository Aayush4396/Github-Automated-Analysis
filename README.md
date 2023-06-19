# Github-Automated-Analysis
Enter a github username to get the name of the technically complex and challenging repo, along with the rationale and complexity score.

Process:
1. Using the GitHub API, after entering a username, all of their public repositories was gathered. 
2. Once all of the repositories, gathering of all of the files in that repo and filtering only the ipynb and py files.
3. After retrieving the code for each file, codecleaning included comment removal, import statements removal, and so on.
4. The GPT API was then prompted and the code was fed to calculate the complexity score and the rationale.
5. After obtaining the scores for all of the codes, I averaged the scores for each repo and requested GPT API for its reasoning once again.
6. Using this method, I gathered the complexity score and rationale, and then returned the repo name with the greatest complexity score and it's rationale.

NOTE: 
1. Currently, due to limitation of GPT api, the code faces the issue of system overload issue due to more number of requests being sent to the api. 
2. I have only checked those repos of a username which contains py or ipynb file.
3. The api tokens of both GitHub and GPT has to be filled if someone is using this code.
4. Finding the complexity of the repo also includes other features such as repo structure which was not taken into consideration.
