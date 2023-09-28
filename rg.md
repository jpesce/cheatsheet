# Rg (ripgrep)

## Find and replace
rg "\.\./string" --files-with-matches | xargs sed -i '' 's/\.\.\/string/newstring/g'
