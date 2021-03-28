# deployments logs 2e84c001114d4ab6a8fc2e7c25d52e1b

```bash
Creating Working Directory
Cloning norbert-config
Cloning into 'norbert-config'...
Cloning into 'norbert-config'...
alva-service/Chart.yaml
alva-service/templates/_helpers.tpl
alva-service/templates/deployment.yaml
alva-service/templates/ingress/_alb.tpl
alva-service/templates/ingress/_nginx.tpl
alva-service/templates/ingress/_traefik.tpl
alva-service/templates/ingress.yaml
alva-service/templates/network_policy.yaml
alva-service/templates/pod_disruption_budget.yaml
alva-service/templates/service.yaml
alva-service/README.md
alva-service/conf/mlconfig.yaml
alva-service/conf/watt.yaml
Creating waypoint.yaml
Initializing kubectl context
Uploading Secrets - watt
2020-12-01T16:01:16.571Z 8 TID-gpn7vn7m4 INFO: type=Class class=BaseAction | source: base_action.rb:69:in `register_sidekiq_queue' | Registering sidekiq_queue=pipeline_trigger
2020-12-01T16:01:16.571Z 8 TID-gpn7vn7m4 INFO: type=Class class=BaseAction | source: base_action.rb:69:in `register_sidekiq_queue' | Registering sidekiq_queue=application_synchronizer
2020-12-01T16:01:16.574Z 8 TID-gpn7vn7m4 INFO: type=Class class=BaseAction | source: base_action.rb:69:in `register_sidekiq_queue' | Registering sidekiq_queue=provider_role_synchronizer
2020-12-01T16:01:16.575Z 8 TID-gpn7vn7m4 INFO: type=Class class=BaseAction | source: base_action.rb:69:in `register_sidekiq_queue' | Registering sidekiq_queue=role_synchronizer
2020-12-01T16:01:16.578Z 8 TID-gpn7vn7m4 INFO: type=Class class=BaseAction | source: base_action.rb:69:in `register_sidekiq_queue' | Registering sidekiq_queue=secret_synchronizer
2020-12-01T16:01:16.579Z 8 TID-gpn7vn7m4 INFO: type=Class class=BaseAction | source: base_action.rb:69:in `register_sidekiq_queue' | Registering sidekiq_queue=template_synchronizer
2020-12-01T16:01:16.655Z 8 TID-gpn7vn7m4 INFO: type=Class class=BaseAction | source: base_action.rb:69:in `register_sidekiq_queue' | Registering sidekiq_queue=namespace_synchronizer
2020-12-01T16:01:16.794Z 8 TID-gpn7vn7m4 INFO: type=Class class=BaseAction | source: base_action.rb:69:in `register_sidekiq_queue' | Registering sidekiq_queue=validator
2020-12-01T16:01:16.926Z 8 TID=gpn7vn7lw INFO: type=Instance class=Model::WaypointConfig id=47147420861920 | source: waypoint_config.rb:88:in `load_yaml' | log_type=configuration Waypoint config file=/config/waypoint.yml doesn't exist, checking for next file.
2020-12-01T16:01:16.926Z 8 TID=gpn7vn7lw INFO: type=Instance class=Model::WaypointConfig id=47147420861920 | source: waypoint_config.rb:85:in `load_yaml' | log_type=configuration Loading waypoint config file=/config/waypoint.yaml.
2020-12-01T16:01:16.927Z 8 TID=gpn7vn7lw INFO: type=Instance class=Model::WaypointConfig id=47147420861920 | source: waypoint_config.rb:88:in `load_yaml' | log_type=configuration Waypoint config file=/config/waypoint-local.yml doesn't exist, checking for next file.
2020-12-01T16:01:16.927Z 8 TID=gpn7vn7lw INFO: type=Instance class=Model::WaypointConfig id=47147420861920 | source: waypoint_config.rb:88:in `load_yaml' | log_type=configuration Waypoint config file=/config/waypoint-local.yaml doesn't exist, checking for next file.
2020-12-01T16:01:16.929Z 8 TID=gpn7vn7lw INFO: type=Class class=ProviderProcessor | source: provider_processor.rb:11:in `register_provider_processor' | log_type=configuration provider=aws is disabled for new processor AwsSpinnakerServiceAccountProcessor with processor_type=spinnakerServiceAccount, ignoring new processor.
2020-12-01T16:01:16.930Z 8 TID=gpn7vn7lw INFO: type=Class class=ProviderProcessor | source: provider_processor.rb:11:in `register_provider_processor' | log_type=configuration provider=dcos is disabled for new processor DcosClouddriverConfigProcessor with processor_type=clouddriverConfig, ignoring new processor.
2020-12-01T16:01:16.935Z 8 TID=gpn7vn7lw INFO: type=Class class=ProviderProcessor | source: provider_processor.rb:11:in `register_provider_processor' | log_type=configuration provider=dcos is disabled for new processor DcosRolesProcessor with processor_type=providerRoles, ignoring new processor.
2020-12-01T16:01:16.935Z 8 TID=gpn7vn7lw INFO: type=Class class=ProviderProcessor | source: provider_processor.rb:11:in `register_provider_processor' | log_type=configuration provider=dcos is disabled for new processor DcosSpinnakerServiceAccountProcessor with processor_type=spinnakerServiceAccount, ignoring new processor.
2020-12-01T16:01:16.936Z 8 TID=gpn7vn7lw INFO: type=Class class=ProviderProcessor | source: provider_processor.rb:11:in `register_provider_processor' | log_type=configuration provider=dockerRegistry is disabled for new processor DockerRegistryClouddriverConfigProcessor with processor_type=clouddriverConfig, ignoring new processor.
2020-12-01T16:01:16.939Z 8 TID=gpn7vn7lw INFO: type=Class class=ProviderProcessor | source: provider_processor.rb:11:in `register_provider_processor' | log_type=configuration provider=github is disabled for new processor GithubRolesProcessor with processor_type=providerRoles, ignoring new processor.
2020-12-01T16:01:16.946Z 8 TID=gpn7vn7lw INFO: type=Class class=ProviderProcessor | source: provider_processor.rb:15:in `register_provider_processor' | log_type=configuration processor_type=clouddriverConfig is disabled for new processor KubeClouddriverConfigProcessor with provider=kube, ignoring new processor.
2020-12-01T16:01:16.952Z 8 TID=gpn7vn7lw INFO: type=Class class=ProviderProcessor | source: provider_processor.rb:15:in `register_provider_processor' | log_type=configuration processor_type=spinnakerServiceAccount is disabled for new processor KubeSpinnakerServiceAccountProcessor with provider=kube, ignoring new processor.
2020-12-01T16:01:16.953Z 8 TID=gpn7vn7lw INFO: type=Class class=ProviderProcessor | source: provider_processor.rb:11:in `register_provider_processor' | log_type=configuration provider=front50 is disabled for new processor Front50RolesProcessor with processor_type=providerRoles, ignoring new processor.
2020-12-01T16:01:16.953Z 8 TID=gpn7vn7lw INFO: type=Class class=ConfigDirectory | source: config_directory.rb:30:in `delete_stale_directories' | Starting deletion of stale config directories. All directories other than [2020-12-01] will be deleted. Current directory is: [/waypoint]
2020-12-01T16:01:22.144Z 8 TID=gpn7vn7lw INFO: type=Instance class=ConfigTree id=47147408215340 | source: config_tree.rb:30:in `initialize' | |-- 'project' alva
|   |-- 'stack' us-gov-1
|   |   |-- 'region' vsphere-kc-k8s-hacas-mid-0
|   |-- 'region' vsphere-kc-k8s-hacas-mid-0
|   |-- 'application' watt
|   |   |-- 'stack' us-gov-1
|   |   |   |-- 'region' vsphere-kc-k8s-hacas-mid-0
2020-12-01T16:01:22.153Z 8 TID=gpn7vn7lw INFO: type=Instance class=StackNode id=47147407485580 | source: config_node.rb:225:in `cryption_base' | Decrypted 6 secrets in file=/home/waypoint/.waypoint/2020-12-01/c16c3037-5c45-4286-b37f-f8c92be0f8ea@local_workspace/config/alva/stack/us-gov-1.
2020-12-01T16:01:22.157Z 8 TID=gpn7vn7lw INFO: type=Instance class=StackNode id=47147407573280 | source: config_node.rb:225:in `cryption_base' | Decrypted 1 secrets in file=/home/waypoint/.waypoint/2020-12-01/c16c3037-5c45-4286-b37f-f8c92be0f8ea@local_workspace/config/alva/app/watt/us-gov-1.
2020-12-01T16:01:22.164Z 8 TID=gpn7vn7lw INFO: type=Instance class=SecretResolver id=47147434877020 | source: secret_resolver.rb:31:in `resolve' | Region info for project=alva application=watt stack=us-gov-1 region=vsphere-kc-k8s-hacas-mid-0: {"all_regions"=>
  #<Set: {"vsphere-ls1-k8s-abl-all-0",
   "open-kc-k8s-corp-alva-0",
   "open-kc-k8s-corp-alva-1",
   "vsphere-emea2-k8s-cernse-all-0",
   "open-kc-k8s-asp-mid-0",
   "open-ls-k8s-asp-mid-0",
   "open-kc-k8s-asp-mid-1",
   "open-ls-k8s-asp-mid-1",
   "open-kc-k8s-asp-mid-2",
   "open-ls-k8s-asp-mid-2",
   "eks-useast2-alvadevusa-ls-test-0",
   "vsphere-kc-k8s-hacas-mid-0"}>,
 "regions_by_stack"=>
  {"abilities-lab-1"=>#<Set: {"vsphere-ls1-k8s-abl-all-0"}>,
   "cert"=>#<Set: {"open-kc-k8s-corp-alva-0"}>,
   "dev"=>#<Set: {"open-kc-k8s-corp-alva-0", "open-kc-k8s-corp-alva-1"}>,
   "emea-2"=>#<Set: {"vsphere-emea2-k8s-cernse-all-0"}>,
   "production"=>
    #<Set: {"open-kc-k8s-asp-mid-0",
     "open-ls-k8s-asp-mid-0",
     "open-kc-k8s-asp-mid-1",
     "open-ls-k8s-asp-mid-1",
     "open-kc-k8s-asp-mid-2",
     "open-ls-k8s-asp-mid-2"}>,
   "sandbox"=>
    #<Set: {"open-ls-k8s-asp-mid-0",
     "open-kc-k8s-asp-mid-0",
     "eks-useast2-alvadevusa-ls-test-0"}>,
   "staging"=>
    #<Set: {"open-ls-k8s-asp-mid-0",
     "open-kc-k8s-asp-mid-0",
     "open-kc-k8s-corp-alva-0",
     "open-kc-k8s-corp-alva-1"}>,
   "us-gov-1"=>#<Set: {"vsphere-kc-k8s-hacas-mid-0"}>},
 "regions_by_tenant"=>{}}

2020-12-01T16:01:22.164Z 8 TID=gpn7vn7lw INFO: type=Instance class=SecretResolver id=47147434877020 | source: secret_resolver.rb:33:in `resolve' | Resolved this hierarchy for valid secrets to deploy for given these targets 
project=alva application=watt stack=us-gov-1 region=vsphere-kc-k8s-hacas-mid-0: 
{:stack=>["us-gov-1"], :region=>["vsphere-kc-k8s-hacas-mid-0"], :tenant=>[]}

2020-12-01T16:01:22.168Z 8 TID=gpn7vn7lw INFO: type=Instance class=SecretResolver id=47147434877020 | source: secret_resolver.rb:40:in `resolve' | Count of different secrets to resolve: 7
More or less than this number may be resolved due to targeting.
2020-12-01T16:01:22.168Z 8 TID=gpn7vn7lw INFO: type=Instance class=SecretResolver id=47147434877020 | source: secret_resolver.rb:145:in `block in add_secret' | Resolved secret=auth-bearer-token with context={:project=>"alva", :application=>nil, :stack=>"us-gov-1", :region=>"vsphere-kc-k8s-hacas-mid-0", :tenant=>nil, :cluster_environment=>"prod", :cluster_provider=>"kube", :name=>"auth-bearer-token"} for region=vsphere-kc-k8s-hacas-mid-0
2020-12-01T16:01:22.169Z 8 TID=gpn7vn7lw INFO: type=Instance class=SecretResolver id=47147434877020 | source: secret_resolver.rb:145:in `block in add_secret' | Resolved secret=consumer-key with context={:project=>"alva", :application=>nil, :stack=>"us-gov-1", :region=>"vsphere-kc-k8s-hacas-mid-0", :tenant=>nil, :cluster_environment=>"prod", :cluster_provider=>"kube", :name=>"consumer-key"} for region=vsphere-kc-k8s-hacas-mid-0
2020-12-01T16:01:22.169Z 8 TID=gpn7vn7lw INFO: type=Instance class=SecretResolver id=47147434877020 | source: secret_resolver.rb:145:in `block in add_secret' | Resolved secret=consumer-secret with context={:project=>"alva", :application=>nil, :stack=>"us-gov-1", :region=>"vsphere-kc-k8s-hacas-mid-0", :tenant=>nil, :cluster_environment=>"prod", :cluster_provider=>"kube", :name=>"consumer-secret"} for region=vsphere-kc-k8s-hacas-mid-0
2020-12-01T16:01:22.169Z 8 TID=gpn7vn7lw INFO: type=Instance class=SecretResolver id=47147434877020 | source: secret_resolver.rb:145:in `block in add_secret' | Resolved secret=new-relic-license-key with context={:project=>"alva", :application=>nil, :stack=>"us-gov-1", :region=>"vsphere-kc-k8s-hacas-mid-0", :tenant=>nil, :cluster_environment=>"prod", :cluster_provider=>"kube", :name=>"new-relic-license-key"} for region=vsphere-kc-k8s-hacas-mid-0
2020-12-01T16:01:22.169Z 8 TID=gpn7vn7lw INFO: type=Instance class=SecretResolver id=47147434877020 | source: secret_resolver.rb:145:in `block in add_secret' | Resolved secret=non-prod-consumer-key with context={:project=>"alva", :application=>nil, :stack=>"us-gov-1", :region=>"vsphere-kc-k8s-hacas-mid-0", :tenant=>nil, :cluster_environment=>"prod", :cluster_provider=>"kube", :name=>"non-prod-consumer-key"} for region=vsphere-kc-k8s-hacas-mid-0
2020-12-01T16:01:22.169Z 8 TID=gpn7vn7lw INFO: type=Instance class=SecretResolver id=47147434877020 | source: secret_resolver.rb:145:in `block in add_secret' | Resolved secret=non-prod-consumer-secret with context={:project=>"alva", :application=>nil, :stack=>"us-gov-1", :region=>"vsphere-kc-k8s-hacas-mid-0", :tenant=>nil, :cluster_environment=>"prod", :cluster_provider=>"kube", :name=>"non-prod-consumer-secret"} for region=vsphere-kc-k8s-hacas-mid-0
2020-12-01T16:01:22.170Z 8 TID=gpn7vn7lw INFO: type=Instance class=SecretResolver id=47147434877020 | source: secret_resolver.rb:145:in `block in add_secret' | Resolved secret=watt-openid-key with context={:project=>"alva", :application=>"watt", :stack=>"us-gov-1", :region=>"vsphere-kc-k8s-hacas-mid-0", :tenant=>nil, :cluster_environment=>"prod", :cluster_provider=>"kube", :name=>"watt-openid-key"} for region=vsphere-kc-k8s-hacas-mid-0
2020-12-01T16:01:22.170Z 8 TID=gpn7vn7lw INFO: type=Instance class=SecretUploader id=47147433750580 | source: secret_uploader.rb:34:in `upload_secret' | Uploading secret=auth-bearer-token, context=project=alva stack=us-gov-1 region=vsphere-kc-k8s-hacas-mid-0
2020-12-01T16:01:22.170Z 8 TID=gpn7vn7lw INFO: type=Class class=KubeClient | source: kube_client.rb:39:in `for' | Creating Kubernetes client for cluster=vsphere-kc-k8s-hacas-mid-0
2020-12-01T16:01:22.170Z 8 TID=gpn7vn7lw INFO: Using configFile: /output/kubeconfig.yaml to build kube client for cluster=vsphere-kc-k8s-hacas-mid-0
2020-12-01T16:01:22.215Z 8 TID=gpn7vn7lw INFO: type=Instance class=KubeClient id=47147433695740 | source: kube_client.rb:82:in `upsert_secret' | Skipping secret upload for secret=us-gov-1.auth-bearer-token. Value hasn't changed.
2020-12-01T16:01:22.215Z 8 TID=gpn7vn7lw INFO: type=Instance class=SecretUploader id=47147433750580 | source: secret_uploader.rb:34:in `upload_secret' | Uploading secret=consumer-key, context=project=alva stack=us-gov-1 region=vsphere-kc-k8s-hacas-mid-0
2020-12-01T16:01:22.228Z 8 TID=gpn7vn7lw INFO: type=Instance class=KubeClient id=47147433695740 | source: kube_client.rb:82:in `upsert_secret' | Skipping secret upload for secret=us-gov-1.consumer-key. Value hasn't changed.
2020-12-01T16:01:22.229Z 8 TID=gpn7vn7lw INFO: type=Instance class=SecretUploader id=47147433750580 | source: secret_uploader.rb:34:in `upload_secret' | Uploading secret=consumer-secret, context=project=alva stack=us-gov-1 region=vsphere-kc-k8s-hacas-mid-0
2020-12-01T16:01:22.243Z 8 TID=gpn7vn7lw INFO: type=Instance class=KubeClient id=47147433695740 | source: kube_client.rb:82:in `upsert_secret' | Skipping secret upload for secret=us-gov-1.consumer-secret. Value hasn't changed.
2020-12-01T16:01:22.243Z 8 TID=gpn7vn7lw INFO: type=Instance class=SecretUploader id=47147433750580 | source: secret_uploader.rb:34:in `upload_secret' | Uploading secret=new-relic-license-key, context=project=alva stack=us-gov-1 region=vsphere-kc-k8s-hacas-mid-0
2020-12-01T16:01:22.257Z 8 TID=gpn7vn7lw INFO: type=Instance class=KubeClient id=47147433695740 | source: kube_client.rb:82:in `upsert_secret' | Skipping secret upload for secret=us-gov-1.new-relic-license-key. Value hasn't changed.
2020-12-01T16:01:22.257Z 8 TID=gpn7vn7lw INFO: type=Instance class=SecretUploader id=47147433750580 | source: secret_uploader.rb:34:in `upload_secret' | Uploading secret=non-prod-consumer-key, context=project=alva stack=us-gov-1 region=vsphere-kc-k8s-hacas-mid-0
2020-12-01T16:01:22.275Z 8 TID=gpn7vn7lw INFO: type=Instance class=KubeClient id=47147433695740 | source: kube_client.rb:82:in `upsert_secret' | Skipping secret upload for secret=us-gov-1.non-prod-consumer-key. Value hasn't changed.
2020-12-01T16:01:22.276Z 8 TID=gpn7vn7lw INFO: type=Instance class=SecretUploader id=47147433750580 | source: secret_uploader.rb:34:in `upload_secret' | Uploading secret=non-prod-consumer-secret, context=project=alva stack=us-gov-1 region=vsphere-kc-k8s-hacas-mid-0
2020-12-01T16:01:22.289Z 8 TID=gpn7vn7lw INFO: type=Instance class=KubeClient id=47147433695740 | source: kube_client.rb:82:in `upsert_secret' | Skipping secret upload for secret=us-gov-1.non-prod-consumer-secret. Value hasn't changed.
2020-12-01T16:01:22.289Z 8 TID=gpn7vn7lw INFO: type=Instance class=SecretUploader id=47147433750580 | source: secret_uploader.rb:34:in `upload_secret' | Uploading secret=watt-openid-key, context=project=alva application=watt stack=us-gov-1 region=vsphere-kc-k8s-hacas-mid-0
2020-12-01T16:01:22.301Z 8 TID=gpn7vn7lw INFO: type=Instance class=KubeClient id=47147433695740 | source: kube_client.rb:82:in `upsert_secret' | Skipping secret upload for secret=watt.us-gov-1.watt-openid-key. Value hasn't changed.
2020-12-01T16:01:22.302Z 8 TID=gpn7vn7lw INFO: type=Instance class=StackNode id=47147407485580 | source: config_node.rb:225:in `cryption_base' | Encrypted 6 secrets in file=/home/waypoint/.waypoint/2020-12-01/c16c3037-5c45-4286-b37f-f8c92be0f8ea@local_workspace/config/alva/stack/us-gov-1.
2020-12-01T16:01:22.306Z 8 TID=gpn7vn7lw INFO: type=Instance class=StackNode id=47147407573280 | source: config_node.rb:225:in `cryption_base' | Encrypted 1 secrets in file=/home/waypoint/.waypoint/2020-12-01/c16c3037-5c45-4286-b37f-f8c92be0f8ea@local_workspace/config/alva/app/watt/us-gov-1.
Generating Config - watt
2020-12-01T16:01:26.683Z 10 TID-gn77bxoi6 INFO: type=Class class=BaseAction | source: base_action.rb:69:in `register_sidekiq_queue' | Registering sidekiq_queue=pipeline_trigger
2020-12-01T16:01:26.684Z 10 TID-gn77bxoi6 INFO: type=Class class=BaseAction | source: base_action.rb:69:in `register_sidekiq_queue' | Registering sidekiq_queue=application_synchronizer
2020-12-01T16:01:26.687Z 10 TID-gn77bxoi6 INFO: type=Class class=BaseAction | source: base_action.rb:69:in `register_sidekiq_queue' | Registering sidekiq_queue=provider_role_synchronizer
2020-12-01T16:01:26.688Z 10 TID-gn77bxoi6 INFO: type=Class class=BaseAction | source: base_action.rb:69:in `register_sidekiq_queue' | Registering sidekiq_queue=role_synchronizer
2020-12-01T16:01:26.691Z 10 TID-gn77bxoi6 INFO: type=Class class=BaseAction | source: base_action.rb:69:in `register_sidekiq_queue' | Registering sidekiq_queue=secret_synchronizer
2020-12-01T16:01:26.692Z 10 TID-gn77bxoi6 INFO: type=Class class=BaseAction | source: base_action.rb:69:in `register_sidekiq_queue' | Registering sidekiq_queue=template_synchronizer
2020-12-01T16:01:26.771Z 10 TID-gn77bxoi6 INFO: type=Class class=BaseAction | source: base_action.rb:69:in `register_sidekiq_queue' | Registering sidekiq_queue=namespace_synchronizer
2020-12-01T16:01:26.919Z 10 TID-gn77bxoi6 INFO: type=Class class=BaseAction | source: base_action.rb:69:in `register_sidekiq_queue' | Registering sidekiq_queue=validator
2020-12-01T16:01:27.049Z 10 TID=gn77bxohw INFO: type=Instance class=Model::WaypointConfig id=46955838640700 | source: waypoint_config.rb:88:in `load_yaml' | log_type=configuration Waypoint config file=/config/waypoint.yml doesn't exist, checking for next file.
2020-12-01T16:01:27.049Z 10 TID=gn77bxohw INFO: type=Instance class=Model::WaypointConfig id=46955838640700 | source: waypoint_config.rb:85:in `load_yaml' | log_type=configuration Loading waypoint config file=/config/waypoint.yaml.
2020-12-01T16:01:27.050Z 10 TID=gn77bxohw INFO: type=Instance class=Model::WaypointConfig id=46955838640700 | source: waypoint_config.rb:88:in `load_yaml' | log_type=configuration Waypoint config file=/config/waypoint-local.yml doesn't exist, checking for next file.
2020-12-01T16:01:27.050Z 10 TID=gn77bxohw INFO: type=Instance class=Model::WaypointConfig id=46955838640700 | source: waypoint_config.rb:88:in `load_yaml' | log_type=configuration Waypoint config file=/config/waypoint-local.yaml doesn't exist, checking for next file.
2020-12-01T16:01:27.052Z 10 TID=gn77bxohw INFO: type=Class class=ProviderProcessor | source: provider_processor.rb:11:in `register_provider_processor' | log_type=configuration provider=aws is disabled for new processor AwsSpinnakerServiceAccountProcessor with processor_type=spinnakerServiceAccount, ignoring new processor.
2020-12-01T16:01:27.053Z 10 TID=gn77bxohw INFO: type=Class class=ProviderProcessor | source: provider_processor.rb:11:in `register_provider_processor' | log_type=configuration provider=dcos is disabled for new processor DcosClouddriverConfigProcessor with processor_type=clouddriverConfig, ignoring new processor.
2020-12-01T16:01:27.057Z 10 TID=gn77bxohw INFO: type=Class class=ProviderProcessor | source: provider_processor.rb:11:in `register_provider_processor' | log_type=configuration provider=dcos is disabled for new processor DcosRolesProcessor with processor_type=providerRoles, ignoring new processor.
2020-12-01T16:01:27.058Z 10 TID=gn77bxohw INFO: type=Class class=ProviderProcessor | source: provider_processor.rb:11:in `register_provider_processor' | log_type=configuration provider=dcos is disabled for new processor DcosSpinnakerServiceAccountProcessor with processor_type=spinnakerServiceAccount, ignoring new processor.
2020-12-01T16:01:27.059Z 10 TID=gn77bxohw INFO: type=Class class=ProviderProcessor | source: provider_processor.rb:11:in `register_provider_processor' | log_type=configuration provider=dockerRegistry is disabled for new processor DockerRegistryClouddriverConfigProcessor with processor_type=clouddriverConfig, ignoring new processor.
2020-12-01T16:01:27.061Z 10 TID=gn77bxohw INFO: type=Class class=ProviderProcessor | source: provider_processor.rb:11:in `register_provider_processor' | log_type=configuration provider=github is disabled for new processor GithubRolesProcessor with processor_type=providerRoles, ignoring new processor.
2020-12-01T16:01:27.063Z 10 TID=gn77bxohw INFO: type=Class class=ProviderProcessor | source: provider_processor.rb:15:in `register_provider_processor' | log_type=configuration processor_type=clouddriverConfig is disabled for new processor KubeClouddriverConfigProcessor with provider=kube, ignoring new processor.
2020-12-01T16:01:27.075Z 10 TID=gn77bxohw INFO: type=Class class=ProviderProcessor | source: provider_processor.rb:15:in `register_provider_processor' | log_type=configuration processor_type=spinnakerServiceAccount is disabled for new processor KubeSpinnakerServiceAccountProcessor with provider=kube, ignoring new processor.
2020-12-01T16:01:27.076Z 10 TID=gn77bxohw INFO: type=Class class=ProviderProcessor | source: provider_processor.rb:11:in `register_provider_processor' | log_type=configuration provider=front50 is disabled for new processor Front50RolesProcessor with processor_type=providerRoles, ignoring new processor.
2020-12-01T16:01:27.077Z 10 TID=gn77bxohw INFO: type=Class class=ConfigDirectory | source: config_directory.rb:30:in `delete_stale_directories' | Starting deletion of stale config directories. All directories other than [2020-12-01] will be deleted. Current directory is: [/waypoint]
2020-12-01T16:01:31.947Z 10 TID=gn77bxohw INFO: type=Instance class=GenerateConfig::GenerateConfigAction id=46955838642000 | source: generate_config.rb:137:in `generate_config' | Generating config for [project=alva, application=watt, stack=us-gov-1, region=vsphere-kc-k8s-hacas-mid-0].
2020-12-01T16:01:31.964Z 10 TID=gn77bxohw INFO: type=Instance class=ConfigTree id=46955845155300 | source: config_tree.rb:30:in `initialize' | |-- 'project' alva
|   |-- 'stack' us-gov-1
|   |   |-- 'region' vsphere-kc-k8s-hacas-mid-0
|   |-- 'region' vsphere-kc-k8s-hacas-mid-0
|   |-- 'application' watt
|   |   |-- 'stack' us-gov-1
|   |   |   |-- 'region' vsphere-kc-k8s-hacas-mid-0
2020-12-01T16:01:32.053Z 10 TID=gn77bxohw INFO: type=Instance class=KubeConfigGenerator id=46955817064480 | source: config_generator.rb:125:in `add_new_relic_id!' | Missing either newrelicAppName or newrelicAccount in config for: project=alva application=watt stack=us-gov-1 region=vsphere-kc-k8s-hacas-mid-0
2020-12-01T16:01:32.196Z 10 TID=gn77bxohw INFO: type=Instance class=KubeConfigGenerator id=46955817064480 | source: kube_config_generator.rb:274:in `block in generate_pod' | Only the CLUSTER operator is currently supported for Kubernetes deployment targets. Skipping constraint='az:GROUP_BY:3'
2020-12-01T16:01:32.196Z 10 TID=gn77bxohw WARN: type=Instance class=KubeConfigGenerator id=46955817064480 | source: kube_config_generator.rb:598:in `generate_network_manifests' | USER networking does not apply in Kubernetes - ignoring
2020-12-01T16:01:32.221Z 10 TID=gn77bxohw INFO: type=Instance class=KubeConfigGenerator id=46955817064480 | source: kube_config_generator.rb:88:in `generate' | Generated Kubernetes manifests for targets project=alva application=watt stack=us-gov-1 region=vsphere-kc-k8s-hacas-mid-0: ---
apiVersion: apps/v1
kind: Deployment
metadata:
  name: watt-us-gov-1
  namespace: alva-prod
  annotations:
    norbert.cerner.com/MCS_POINTS_OF_CONTACT: matt.nelson@cerner.com,gabe.henkes@cerner.com,scott.buchholz@cerner.com,naresh.rayapati@cerner.com
    norbert.cerner.com/com.cerner.repo_sha: e9ec93a359b3218e3c9b725ff32822fa2d4144a1
    norbert.cerner.com/com.cerner.repo_url: https://github.cerner.com/alva/alva
    norbert.cerner.com/MCS_project: alva
    norbert.cerner.com/MCS_application: watt
    norbert.cerner.com/MCS_stack: us-gov-1
    norbert.cerner.com/MCS_region: vsphere-kc-k8s-hacas-mid-0
    norbert.cerner.com/splunk-index: app_hacas_mcsp_alva
    norbert.cerner.com/splunk-source: alva:watt:us-gov-1:vsphere-kc-k8s-hacas-mid-0:0.68-java11-20201105T181349Z
  labels:
    norbert.cerner.com/project: alva
    norbert.cerner.com/application: watt
    norbert.cerner.com/stack: us-gov-1
    norbert.cerner.com/region: vsphere-kc-k8s-hacas-mid-0
spec:
  revisionHistoryLimit: 1
  selector:
    matchLabels:
      norbert.cerner.com/project: alva
      norbert.cerner.com/application: watt
      norbert.cerner.com/stack: us-gov-1
      norbert.cerner.com/region: vsphere-kc-k8s-hacas-mid-0
  template:
    metadata:
      annotations:
        norbert.cerner.com/MCS_POINTS_OF_CONTACT: matt.nelson@cerner.com,gabe.henkes@cerner.com,scott.buchholz@cerner.com,naresh.rayapati@cerner.com
        norbert.cerner.com/com.cerner.repo_sha: e9ec93a359b3218e3c9b725ff32822fa2d4144a1
        norbert.cerner.com/com.cerner.repo_url: https://github.cerner.com/alva/alva
        norbert.cerner.com/MCS_project: alva
        norbert.cerner.com/MCS_application: watt
        norbert.cerner.com/MCS_stack: us-gov-1
        norbert.cerner.com/MCS_region: vsphere-kc-k8s-hacas-mid-0
        norbert.cerner.com/splunk-index: app_hacas_mcsp_alva
        norbert.cerner.com/splunk-source: alva:watt:us-gov-1:vsphere-kc-k8s-hacas-mid-0:0.68-java11-20201105T181349Z
      labels:
        norbert.cerner.com/project: alva
        norbert.cerner.com/application: watt
        norbert.cerner.com/stack: us-gov-1
        norbert.cerner.com/region: vsphere-kc-k8s-hacas-mid-0
        norbert.cerner.com/profile: alva-watt-us-gov-1
        norbert.cerner.com/exposeTo-alva-watt-us-gov-1: 'true'
        norbert.cerner.com/consume-alva-eureka-us-gov-1-kc3hesxn4-az1-main: 'true'
        norbert.cerner.com/consume-alva-eureka-us-gov-1-kc3hesxn5-az2-main: 'true'
        norbert.cerner.com/consume-alva-eureka-us-gov-1-kc3hesxn6-az3-main: 'true'
        norbert.cerner.com/external-new-relic: 'true'
        norbert.cerner.com/external-associates.cerner.com: 'true'
        norbert.cerner.com/external-us-gov-1-base-network: 'true'
    spec:
      containers:
      - name: watt
        image: docker-secure.cernerrepos.net/alva/alva-watt:0.68-java11-20201105T181349Z
        resources:
          requests:
            cpu: 0.1
            memory: 1264Mi
          limits:
            memory: 1264Mi
        envFrom:
        - configMapRef:
            name: watt-us-gov-1-config
        volumeMounts:
        - name: temp-storage
          mountPath: "/tmp/alva/"
        env:
        - name: NEW_RELIC_LICENSE_KEY
          valueFrom:
            secretKeyRef:
              name: us-gov-1.new-relic-license-key
              key: value
        - name: alva.client.alva-ml-config.token
          valueFrom:
            secretKeyRef:
              name: us-gov-1.auth-bearer-token
              key: value
        - name: alva.watt.openId.key
          valueFrom:
            secretKeyRef:
              name: watt.us-gov-1.watt-openid-key
              key: value
        - name: NEW_RELIC_METADATA_KUBERNETES_CLUSTER_NAME
          value: vsphere-kc-k8s-hacas-mid-0
        - name: NEW_RELIC_METADATA_KUBERNETES_NODE_NAME
          valueFrom:
            fieldRef:
              fieldPath: spec.nodeName
        - name: NEW_RELIC_METADATA_KUBERNETES_NAMESPACE_NAME
          valueFrom:
            fieldRef:
              fieldPath: metadata.namespace
        - name: NEW_RELIC_METADATA_KUBERNETES_DEPLOYMENT_NAME
          valueFrom:
            fieldRef:
              fieldPath: metadata.annotations['artifact.spinnaker.io/name']
        - name: NEW_RELIC_METADATA_KUBERNETES_POD_NAME
          valueFrom:
            fieldRef:
              fieldPath: metadata.name
        - name: NEW_RELIC_METADATA_KUBERNETES_CONTAINER_NAME
          valueFrom:
            fieldRef:
              fieldPath: metadata.annotations['moniker.spinnaker.io/application']
        - name: NEW_RELIC_METADATA_KUBERNETES_CONTAINER_IMAGE_NAME
          value: docker-secure.cernerrepos.net/alva/alva-watt:0.68-java11-20201105T181349Z
        readinessProbe:
          periodSeconds: 30
          timeoutSeconds: 10
          httpGet:
            path: "/meta/health"
            port: main
            scheme: HTTPS
        livenessProbe:
          initialDelaySeconds: 600
          periodSeconds: 30
          timeoutSeconds: 10
          httpGet:
            path: "/meta/availability"
            port: main
            scheme: HTTPS
        ports:
        - containerPort: 8443
          name: main
          protocol: TCP
        - containerPort: 8444
          name: admin
          protocol: TCP
        lifecycle:
          preStop:
            exec:
              command:
              - sleep
              - '10'
      priorityClassName: high
      securityContext:
        runAsUser: 0
      volumes:
      - name: temp-storage
        emptyDir: {}
  replicas: 2

---
apiVersion: extensions/v1beta1
kind: Ingress
metadata:
  name: watt-us-gov-1-main-nginx
  namespace: alva-prod
  annotations:
    kubernetes.io/ingress.class: nginx
    nginx.ingress.kubernetes.io/backend-protocol: HTTPS
    certmanager.k8s.io/cluster-issuer: default-self-signing-issuer
  labels:
    norbert.cerner.com/project: alva
    norbert.cerner.com/application: watt
    norbert.cerner.com/stack: us-gov-1
    norbert.cerner.com/region: vsphere-kc-k8s-hacas-mid-0
spec:
  tls:
  - hosts:
    - watt-alva-us-gov-1.vsphere-kc-k8s-hacas-mid-0.cernerhacas.net
    secretName: watt-alva-us-gov-1-vsphere-kc-k8s-hacas-mid-0-cernerhacas-net
  rules:
  - host: watt-alva-us-gov-1.vsphere-kc-k8s-hacas-mid-0.cernerhacas.net
    http:
      paths:
      - backend:
          serviceName: watt-us-gov-1-service
          servicePort: 8443

---
apiVersion: extensions/v1beta1
kind: Ingress
metadata:
  name: watt-us-gov-1-main-traefik
  namespace: alva-prod
  annotations:
    kubernetes.io/ingress.class: traefik
    ingress.kubernetes.io/protocol: https
    certmanager.k8s.io/cluster-issuer: default-self-signing-issuer
  labels:
    norbert.cerner.com/project: alva
    norbert.cerner.com/application: watt
    norbert.cerner.com/stack: us-gov-1
    norbert.cerner.com/region: vsphere-kc-k8s-hacas-mid-0
spec:
  tls:
  - hosts:
    - watt-alva-us-gov-1.vsphere-kc-k8s-hacas-mid-0.cernerhacas.net
    secretName: watt-alva-us-gov-1-vsphere-kc-k8s-hacas-mid-0-cernerhacas-net
  rules:
  - host: watt-alva-us-gov-1.vsphere-kc-k8s-hacas-mid-0.cernerhacas.net
    http:
      paths:
      - backend:
          serviceName: watt-us-gov-1-service
          servicePort: 8443

---
kind: Service
apiVersion: v1
metadata:
  name: watt-us-gov-1-service
  namespace: alva-prod
  labels:
    norbert.cerner.com/project: alva
    norbert.cerner.com/application: watt
    norbert.cerner.com/stack: us-gov-1
    norbert.cerner.com/region: vsphere-kc-k8s-hacas-mid-0
spec:
  selector:
    norbert.cerner.com/project: alva
    norbert.cerner.com/application: watt
    norbert.cerner.com/stack: us-gov-1
    norbert.cerner.com/region: vsphere-kc-k8s-hacas-mid-0
  ports:
  - name: main
    protocol: TCP
    port: 8443
    targetPort: main

---
apiVersion: networking.k8s.io/v1
kind: NetworkPolicy
metadata:
  name: exposeto-ingress-alva-watt-us-gov-1
  namespace: alva-prod
  labels:
    norbert.cerner.com/project: alva
    norbert.cerner.com/application: watt
    norbert.cerner.com/stack: us-gov-1
    norbert.cerner.com/region: vsphere-kc-k8s-hacas-mid-0
spec:
  policyTypes:
  - Ingress
  podSelector:
    matchLabels:
      norbert.cerner.com/exposeTo-alva-watt-us-gov-1: 'true'
  ingress:
  - from:
    - podSelector:
        matchLabels:
          norbert.cerner.com/profile: alva-watt-us-gov-1
    ports: []

---
apiVersion: networking.k8s.io/v1
kind: NetworkPolicy
metadata:
  name: exposeto-egress-alva-watt-us-gov-1
  namespace: alva-prod
  labels:
    norbert.cerner.com/project: alva
    norbert.cerner.com/application: watt
    norbert.cerner.com/stack: us-gov-1
    norbert.cerner.com/region: vsphere-kc-k8s-hacas-mid-0
spec:
  policyTypes:
  - Egress
  podSelector:
    matchLabels:
      norbert.cerner.com/profile: alva-watt-us-gov-1
  egress:
  - to:
    - podSelector:
        matchLabels:
          norbert.cerner.com/exposeTo-alva-watt-us-gov-1: 'true'
    ports: []

---
apiVersion: networking.k8s.io/v1
kind: NetworkPolicy
metadata:
  name: external-new-relic
  namespace: alva-prod
  labels:
    norbert.cerner.com/project: alva
    norbert.cerner.com/application: watt
    norbert.cerner.com/stack: us-gov-1
    norbert.cerner.com/region: vsphere-kc-k8s-hacas-mid-0
spec:
  policyTypes:
  - Egress
  podSelector:
    matchLabels:
      norbert.cerner.com/external-new-relic: 'true'
  egress:
  - to:
    - ipBlock:
        cidr: 50.31.164.0/24
    - ipBlock:
        cidr: 162.247.240.0/22
    ports:
    - port: 443
      protocol: TCP

---
apiVersion: networking.k8s.io/v1
kind: NetworkPolicy
metadata:
  name: external-associates.cerner.com
  namespace: alva-prod
  labels:
    norbert.cerner.com/project: alva
    norbert.cerner.com/application: watt
    norbert.cerner.com/stack: us-gov-1
    norbert.cerner.com/region: vsphere-kc-k8s-hacas-mid-0
spec:
  policyTypes:
  - Egress
  podSelector:
    matchLabels:
      norbert.cerner.com/external-associates.cerner.com: 'true'
  egress:
  - to:
    - ipBlock:
        cidr: 159.140.206.11/32
    ports:
    - port: 443
      protocol: TCP

---
apiVersion: networking.k8s.io/v1
kind: NetworkPolicy
metadata:
  name: external-us-gov-1-base-network
  namespace: alva-prod
  labels:
    norbert.cerner.com/project: alva
    norbert.cerner.com/application: watt
    norbert.cerner.com/stack: us-gov-1
    norbert.cerner.com/region: vsphere-kc-k8s-hacas-mid-0
spec:
  policyTypes:
  - Egress
  podSelector:
    matchLabels:
      norbert.cerner.com/external-us-gov-1-base-network: 'true'
  egress:
  - to:
    - ipBlock:
        cidr: 172.0.0.0/8
    ports:
    - port: 80
      protocol: TCP
    - port: 8080
      protocol: TCP
    - port: 389
      protocol: TCP
    - port: 443
      protocol: TCP
    - port: 636
      protocol: TCP
    - port: 1414
      protocol: TCP
    - port: 1415
      protocol: TCP
    - port: 1416
      protocol: TCP
    - port: 1417
      protocol: TCP
    - port: 1418
      protocol: TCP
    - port: 1419
      protocol: TCP
    - port: 1420
      protocol: TCP
    - port: 1421
      protocol: TCP
    - port: 1521
      protocol: TCP

---
apiVersion: networking.k8s.io/v1
kind: NetworkPolicy
metadata:
  name: allow-ingress-watt-us-gov-1
  namespace: alva-prod
  labels:
    norbert.cerner.com/project: alva
    norbert.cerner.com/application: watt
    norbert.cerner.com/stack: us-gov-1
    norbert.cerner.com/region: vsphere-kc-k8s-hacas-mid-0
spec:
  podSelector:
    matchLabels:
      norbert.cerner.com/project: alva
      norbert.cerner.com/application: watt
      norbert.cerner.com/stack: us-gov-1
      norbert.cerner.com/region: vsphere-kc-k8s-hacas-mid-0
  policyTypes:
  - Ingress
  ingress:
  - from:
    - namespaceSelector:
        matchLabels:
          name: ingress-nginx
    - namespaceSelector:
        matchLabels:
          name: ingress
    ports:
    - protocol: TCP
      port: 8443
  - from:
    - namespaceSelector:
        matchLabels:
          name: ingress-traefik
    - namespaceSelector:
        matchLabels:
          name: ingress
    ports:
    - protocol: TCP
      port: 8443

---
apiVersion: v1
kind: ConfigMap
metadata:
  name: watt-us-gov-1-config
  namespace: alva-prod
  annotations:
    strategy.spinnaker.io/max-version-history: '2'
  labels:
    norbert.cerner.com/project: alva
    norbert.cerner.com/application: watt
    norbert.cerner.com/stack: us-gov-1
    norbert.cerner.com/region: vsphere-kc-k8s-hacas-mid-0
data:
  alva.keystore.cert.alias: alva_2018
  busyBoxRepo: docker-secure.cernerrepos.net
  certificateClientImage: norbert/ca-certs-client:v0.4.1
  certificateClientRepo: docker-secure.cernerrepos.net
  JAVA_OPTS: "-Xms512m -Xmx512m -Xss256k -XX:MaxMetaspaceSize=256m -Dcom.sun.management.jmxremote.port=8082 -Dcom.sun.management.jmxremote.rmi.port=8082 -Dcom.sun.management.jmxremote.ssl=false -Dcom.sun.management.jmxremote.authenticate=false -XX:+UseG1GC -XX:+UseStringDeduplication -XX:MaxGCPauseMillis=150 -XX:+UnlockDiagnosticVMOptions -XX:+DebugNonSafepoints -XX:+HeapDumpOnOutOfMemoryError -XX:HeapDumpPath=/tmp/alva/$NEW_RELIC_METADATA_KUBERNETES_CONTAINER_NAME.hprof -XX:+ExitOnOutOfMemoryError -Djava.security.egd=file:/dev/./urandom -javaagent:/opt/newrelic/newrelic.jar -Dcom.cerner.system.instrument.logging.jdk.logging.logDiagnosticTexts=true -Dcom.cerner.system.instrument.logging.jdk.tracing.logDiagnosticTexts=true -Djavax.net.ssl.trustStore=/opt/alva/ca-certs/alva-ca-certificates.jks"
  NEW_RELIC_APP_NAME: alva-watt_us-gov-1
  alva.dataCenter.type: override-project-default
  alva.logging.com.netflix.discovery.shared.resolver.aws.ConfigClusterResolver: WARN
  alva.logging.org.eclipse.jetty.server.HttpChannelState: ERROR
  com.cerner.system.enterprise.client.arctic.interface.cache.expire: '900'
  eureka.port: '8080'
  eureka.port.enabled: 'false'
  eureka.securePort: '8443'
  eureka.securePort.enabled: 'true'
  eureka.serviceUrl.default: http://eureka-us-gov-1-kc3hesxn4-az1-service.alva-prod.svc.cluster.local:8080/v2,http://eureka-us-gov-1-kc3hesxn5-az2-service.alva-prod.svc.cluster.local:8080/v2,http://eureka-us-gov-1-kc3hesxn6-az3-service.alva-prod.svc.cluster.local:8080/v2
  eureka.shouldEnforceRegistrationAtInit: 'true'
  newrelic.config.labels: platform:Alva;environment:us-gov-1;tier:mid
  NEW_RELIC_CA_BUNDLE_PATH: "/opt/alva/ca-certs/alva-ca-certificates.pem"
  alva.client.socket.tls.trust.all: 'true'
  alva.watt.openId.url: https://associates.cerner.com/accounts/
  eureka.name: alva-watt
  eureka.secureVipAddress: alva-watt
  eureka.transport.applicationsResolverUseIp: 'true'
  hystrix.command.default.execution.isolation.thread.timeoutInMilliseconds: '5000'
  hystrix.command.watt-client.execution.isolation.thread.timeoutInMilliseconds: '60000'

Applying Helm template - watt
```

