# SlashNext Phishing Incident Response for Resilient

SlashNext Phishing Incident Response integration for IBM Resilient 
SOAR platform is a collection of functions that connect to SlashNext's 
On-demand Threat Intelligence (OTI) external APIs. These functions are 
also accompanied with individual Resilient workflows that demonstrate 
the use of each function. These workflows can then be triggered by 
Resilient rules to triage individual Indicators of Compromise (IoC). 
The extension package is bundled with all of these components 
(functions, workflows, rules). In addition to this: workflows, 
rules and script to define the complete business logic of SlashNext's 
playbooks is also packaged within the extension to orchestrate the 
security incident response activities. 

## Requirements 
1. Resilient Appliance platform>=**v35.2.32**
2. Resilient Integration server running:
    * **resilient_circuits>=30.0.0**
    * **resilient_lib>=35.0.203**

## Installation

        It is recommended that you perform all of the steps below 
        in a separate virtual environment as recommended by IBM Resilient

To install SlashNext extension into IBM Resilient platform, 
follow the steps below:

1. Download the **fn_slashnext.zip** file from IBM App Exchange.

2. Copy the **.zip** file to your integration server and SSH into it.

3. **Unzip** the package as follows:

        $  unzip fn_slashnext-x.x.x.zip

4. **Change Directory** into the unzipped directory:

        $  cd fn_slashnext-x.x.x

5. **Install** the package using:

        $  pip install fn_slashnext-x.x.x.tar.gz

6. Next, import the functions, example rules and workflows into 
your Resilient Appliance as follows:

        $  resilient-circuits customize -y -l fn-slashnext

7. To add and update your **app.config** file with the required 
SlashNext configurations, run the following command:

        $  resilient-circuits config -u

8. Then to enter your configurations, open the **app.config** file 
and edit values under **fn_slashnext** section:

        $  vi ~/.resilient/app.config        

        [fn_slashnext]
        snx_base_url=https://oti.slashnext.cloud/api
        snx_api_key=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
        
    **snx_base_url** refers to the SlashNext endpoint URL. Do not changes 
    its value from the default one until or unless specified by SlashNext.
    Insert the SlashNext API key 32-character value assigned to you by 
    SlashNext in **snx_api_key** parameter.

9. Save and close the **app.config** file

10. Finally, run resilient-circuits to load the new changes:

        $  resilient-circuits run
        
        
## Uninstall
        
To uninstall the extension, follow the steps below:

1. SSH into your integration server

2. Uninstall the extension package as follows:

       $  pip uninstall fn-slashnext

3. Open your **app.config** file, scroll to the **fn_slashnext**
section and remove it.
    
4. Save and close the **app.config** file

## Documentation

For a detailed overview of the functions, workflows, scripts and rules
packaged in the extension, refer to the customer guide documentation. 

## Changelog
### 1.0.0
First version SlashNext Phishing Incident Response for Resilient
