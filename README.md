# Batch RPM processing scripts for Terra

Quick scripts for batch-processing of packages in Subatomic repositories.

Now that we have hundreds of packages in Subatomic, and sometimes manual intervention is required to please the repology gods,
I needed a way to batch-process packages to clean up the mess once in a while.

Also note that these scripts are in Fish shell. Because I like using Fish. That's it.

## Usage

1. Get a Subatomic token
2. Create a Subatomic config file in `~/.config/subatomic.json` with the token and API endpoint
3. Run the script.

## Scripts

- `satm-grepdel.fish` - Deletes all package specs that match a certain grep pattern from multiple repositories.
  Works by iterating through each repository, listing all the packages and grepping for the pattern, Then pipes
  that to another function that iterates through all those packages and deletes them. Takes in a pattern as an argument.
