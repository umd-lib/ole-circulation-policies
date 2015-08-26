# ole-circulation-policies
Circulation policy rule files for import into OLE.

This repository contains Drools rules files representing the University of
Maryland library circulation policies for use with Kuali OLE.

These files can be directly imported into OLE using the "Circulation Policy
Ingester" in the "Circulation New' section of the "Deliver" tab.

The files can also be added to the /home/ole/kuali/kuali/main/local/olefs-webapp/rules/
directory. OLE can then be to reload the rules by changing the "LOAD_CIRC_POLICIES_IND"
parameter to "Y", and then performing a circulation action.

These rules are for OLE v1.6.2 and later. Prior to v1.6.2, the KRMS rules engine
was used for circulation policies. The University of Maryland KRMS ruleset has
been moved to the "krms_ruleset" branch.

##Helpful Resources

 * https://wiki.kuali.org/display/OLE/Implementing+Library+Circulation+Policies+Using+Drools

 
## File Organization

Each folder corresponds to a different circulation rule subsets.action.


## OLE Setup

The following permissions must be added to OLE, in order for certain overrides to function:

| Template Namespace | Template Name | Permission Namespace | Permission Name | Granted to Roles |
| ------------------ | ------------- | -------------------- | --------------- | ---------------- |
| KUALI | Default | OLE-DLVR | Item does not circulate | OLE-PTRN Super Circulation Supervisor |
| KUALI | Default | OLE-DLVR | Patron type not allowed to borrow item type | OLE-PTRN Super Circulation Supervisor |

The following fixed due dates need to be specified:

| Circulation Policy Set | Notes |
| ---------------------- | ----- |
| CHECKOUT_FIXED_DUE_DATE_FAC_STAFF_01 | For Faculty or Staff checking out item type 01 |
| CHECKOUT_FIXED_DUE_DATE_GRAD_01 | For Graduate students checking out item type 01 |


## License

These files are provided under the CC0 1.0 Universal license (http://creativecommons.org/publicdomain/zero/1.0/).
