```
    1  ls
    2  az
    3  sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
    4  sudo sh -c 'echo -e "[azure-cli]
name=Azure CLI
baseurl=https://packages.microsoft.com/yumrepos/azure-cli
enabled=1
gpgcheck=1
gpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
    5  sudo yum install azure-cli
    6  az login
    7  az devops
    8  az extension add --name anextension
    9  az extension add --name devops
   10  az extension add --name azdevops
   11  az artifacts universal download   --organization "https://dev.azure.com/DevOps-Batches/"   --project "f4b641c1-99db-46d1-8110-5c6c24ce2fb9"   --scope project   --feed "devopsb52"   --name "cart"   --version "0.0.1"   --path .
   12  az devops login
   13  az artifacts universal download   --organization "https://dev.azure.com/DevOps-Batches/"   --project "f4b641c1-99db-46d1-8110-5c6c24ce2fb9"   --scope project   --feed "devopsb52"   --name "cart"   --version "0.0.1"   --path .
   14  sudo yum install libicu -y
   15  az artifacts universal download   --organization "https://dev.azure.com/DevOps-Batches/"   --project "f4b641c1-99db-46d1-8110-5c6c24ce2fb9"   --scope project   --feed "devopsb52"   --name "cart"   --version "0.0.1"   --path .
   16  az artifacts universal download   --organization "https://dev.azure.com/DevOps-Batches/"   --project "f4b641c1-99db-46d1-8110-5c6c24ce2fb9"   --scope project   --feed "devopsb52"   --name "cart"   --version "*"   --path .
   17  curl -s https://feeds.dev.azure.com/DevOps-Batches/DevOps52/_apis/packaging/Feeds/cart/packages?api-version=6.1-preview.1
   18  curl https://feeds.dev.azure.com/DevOps-Batches/DevOps52/_apis/packaging/Feeds/devopsb52/packages?api-version=6.1-preview.1
   19  curl https://feeds.dev.azure.com/DevOps-Batches/DevOps52/_apis/packaging/Feeds/devopsb52/packages?api-version=6.1-preview.1 | jq
   20  curl https://feeds.dev.azure.com/DevOps-Batches/DevOps52/_apis/packaging/Feeds/devopsb52/Packages/bb8fe680-1e3b-4cfe-a042-7ab7f9708607/versions?api-version=6.1-preview.1
   21  curl https://feeds.dev.azure.com/DevOps-Batches/DevOps52/_apis/packaging/Feeds/devopsb52/Packages/bb8fe680-1e3b-4cfe-a042-7ab7f9708607/versions?api-version=6.1-preview.1 | jq
   22  curl https://feeds.dev.azure.com/DevOps-Batches/DevOps52/_apis/packaging/Feeds/devopsb52/Packages/bb8fe680-1e3b-4cfe-a042-7ab7f9708607/versions?api-version=6.1-preview.1 | jq '.value[]'
   23  curl https://feeds.dev.azure.com/DevOps-Batches/DevOps52/_apis/packaging/Feeds/devopsb52/Packages/bb8fe680-1e3b-4cfe-a042-7ab7f9708607/versions?api-version=6.1-preview.1 | jq '.value[].version'
   24  curl https://feeds.dev.azure.com/DevOps-Batches/DevOps52/_apis/packaging/Feeds/devopsb52/Packages/bb8fe680-1e3b-4cfe-a042-7ab7f9708607/versions?api-version=6.1-preview.1 | jq '.value[] | .value'
   25  curl https://feeds.dev.azure.com/DevOps-Batches/DevOps52/_apis/packaging/Feeds/devopsb52/Packages/bb8fe680-1e3b-4cfe-a042-7ab7f9708607/versions?api-version=6.1-preview.1 | jq '.value[] | .version'
   26  curl https://feeds.dev.azure.com/DevOps-Batches/DevOps52/_apis/packaging/Feeds/devopsb52/Packages/bb8fe680-1e3b-4cfe-a042-7ab7f9708607/versions?api-version=6.1-preview.1 | jq '.value[] | .version .views'
   27  curl https://feeds.dev.azure.com/DevOps-Batches/DevOps52/_apis/packaging/Feeds/devopsb52/Packages/bb8fe680-1e3b-4cfe-a042-7ab7f9708607/versions?api-version=6.1-preview.1 | jq '.value[] | .version .views[]'
   28  curl https://feeds.dev.azure.com/DevOps-Batches/DevOps52/_apis/packaging/Feeds/devopsb52/Packages/bb8fe680-1e3b-4cfe-a042-7ab7f9708607/versions?api-version=6.1-preview.1 | jq '.value[] | .version .views[].name'
   29  curl https://feeds.dev.azure.com/DevOps-Batches/DevOps52/_apis/packaging/Feeds/devopsb52/Packages/bb8fe680-1e3b-4cfe-a042-7ab7f9708607/versions?api-version=6.1-preview.1 | jq '.value[] | .version+ .views[].name'
   30  curl https://feeds.dev.azure.com/DevOps-Batches/DevOps52/_apis/packaging/Feeds/devopsb52/Packages/bb8fe680-1e3b-4cfe-a042-7ab7f9708607/versions?api-version=6.1-preview.1 | jq '.value[] | .version+ " " +.views[].name'
   31  curl https://feeds.dev.azure.com/DevOps-Batches/DevOps52/_apis/packaging/Feeds/devopsb52/Packages/bb8fe680-1e3b-4cfe-a042-7ab7f9708607/versions?api-version=6.1-preview.1 | jq '.value[] | .version+ " " +.views[].name' | grep Release
   32  curl https://feeds.dev.azure.com/DevOps-Batches/DevOps52/_apis/packaging/Feeds/devopsb52/Packages/bb8fe680-1e3b-4cfe-a042-7ab7f9708607/versions?api-version=6.1-preview.1 | jq '.value[] | .version+ " " +.views[].name' | grep Prerelease
   33  curl https://feeds.dev.azure.com/DevOps-Batches/DevOps52/_apis/packaging/Feeds/devopsb52/Packages/bb8fe680-1e3b-4cfe-a042-7ab7f9708607/versions?api-version=6.1-preview.1 | jq '.value[] | .version+ " " +.views[].name' | grep Local
   34  curl https://feeds.dev.azure.com/DevOps-Batches/DevOps52/_apis/packaging/Feeds/devopsb52/Packages/bb8fe680-1e3b-4cfe-a042-7ab7f9708607/versions?api-version=6.1-preview.1 | jq '.value[] | .version+ " " +.views[].name' | grep Local | head -1
   35  history
```