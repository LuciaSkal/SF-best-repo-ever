# SF-best-repo-ever

1.Enable Dev Hub in your Trailhead Playground

2.If you haven't already done so, authorize your hub org and provide it with an alias (myhuborg in the command below):
sf org login web -d -a myhuborg

3.Clone the lwc-recipes repository:
git clone https://github.com/trailheadapps/lwc-recipes
cd lwc-recipes

4.Create a scratch org and provide it with an alias (lwc-recipes in the command below):
sf org create scratch -d -f config/project-scratch-def.json -a lwc-recipes

5.Push the app to your scratch org:
sf project deploy start

6.Assign the recipes permission set to the default user:
sf org assign permset -n recipes

7.Import sample data:
sf data tree import -p ./data/data-plan.json

8.Open the scratch org:
sf org open