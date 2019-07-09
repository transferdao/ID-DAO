# IdentityDAO 

## Add Identity

### GoodDollar User Onboarding

![](./docs/img/GoodDollar_Wireframe_Add_Identity.png)

After the user goes through GoodDollar's login in / create account flow, they'll be asked to verify their identity. The user will be asked to provide a selfie, video, and social account verifications. These will all be verified by the DAO through a proposal accessible through alchemy.

Example Proposal Payload:
```json
{
  "name" : "Ori Shimony",
  "address" : "0x6230204B1714C691804D1c71F325FDb0e184339Q", 
  "media": {
    "selfie" : "ipfs://ijnyttg6th7y7f5g",
    "video" : "ipfs://NUAh08hniaksm,laks",
  },
  "social" : {
    "Twitter" : "https://twitter.com/dOrg_tech/status/1110270197665951744",
    "LinkedIn" : "...",
    "Github" : "...",
  },
  "oracles" : [
    "GoodDollar",
    "Keybase",
  ]
}
```

Example Oracle Query:
```json
Oracle:
"GoodDollar" => "https://verify.gooddollar.org/0x6230204B1714C691804D1c71F325FDb0e184339Q"
returns:
{
  "facebook-oauth" : true,
  "google-oauth" : true,
  "gov-id-verified" : true
}
```

### Alchemy Identity Verification

![](./docs/img/Alchemy-Add-Identity.png)

In Alchemy, the proposal payload that was prepared in the GoodDollar app is shown in the UI. Any verifications from GoodDollar's oracle are queried by Alchemy and shown. Two primary use cases for this oracle are government ID verification and external account OAuths. With this information, human voters can check these to determine whether the proposal is real. 

### Scenario Flowchart

![](./docs/img/Scenario_Flow_Onboarding_Add_Identity.png)

### Exception Scenarios

Some of the scenarios below may be encountered along the above process and have been briefly fleshed out below. These include a user with a current account already existing on the GoodDollar server attempting to re-register, and a user that has submitted a proposal, but has had it rejected by the DAO.

![](./docs/img/Scenario_Flow_Exception_Existing_User_Attempting_to_Register.png)

![](./docs/img/Scenario_Flow_Exception_User_with_Rejected_Add_Proposal.png)


## Updating Identity

### GoodDollar Edit Identity

![](./docs/img/GoodDollar_Wireframe_Update_Identity.png)

### GoodDollar User Update Process

![](./docs/img/GoodDollar_Wireframe_Update_Identity.png)

### Alchemy Edit Verification

![](./docs/img/Alchemy-Edit-Identity.png)

On Alchemy, any changes or edits to a pre-existing identity will be reflected by the UI. Anything that has stayed the same will be omitted.

### Scenario Flowchart

![](./docs/img/Scenario_Flow_Updating_Edit_Identity.png)

### Exception Scenarios

A rejected proposal to edit a user's information by the DAO is treated much like a rejected proposal to add a user, and is reflected in a very similar way user-side.

![](./docs/img/Scenario_Flow_Exception_User_with_Rejected_Edit_Proposal.png)

## Remove Identity

### GoodDollar User Off-boarding

![](./docs/img/GoodDollar_Wireframe_Delete_Identity.png)

Removing an identity from the GoodDollar app is fairly straightforward. Within the GoodDollar app's menu bar, the user would simply tap "Delete Account", and confirm the deletion. Finally, the GoodDollar server relays the signed transaction to remove the account to the network, and an email is sent to the user on success.

### Scenario Flowchart

![](./docs/img/Scenario_Flow_Offboarding_Delete_Identity.png)

## Miscellaneous Scenarios

### User Forgot PIN

![](./docs/img/Scenario_Flow_Exception_User_Forgot_PIN.png)

### Contact Support

![](./docs/img/Scenario_Flow_Contact_Support.png)

### DAO Removes GoodDollar User's Identity

![](./docs/img/Scenario_Flow_Exception_DAO_Removes_User.png)
