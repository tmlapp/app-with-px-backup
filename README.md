# Deploy an application with a px-backup job/schedule

Edit the deploy_app.yaml file and edit the `vars` section for your environment:
```
  vars:
    debug: false
    app:
      namespace: <namespace of your app>
    kubeconfig: <path to your kubeconfig>
    pxbackup:
      user: admin
      password: <your px-backup ui password>
      ui: <px-backup-ui url>
      api: <px-backup api url>
      name: <name for schedule policy and backup schedule>
      orgid: default
      backuplocation: <your backup location name>
      cluster: <your cluster name>
```

Run the ansible playbook
```
ansible-playbook deploy_app.yaml
```
