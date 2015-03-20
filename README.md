# ole-circulation-policies
Circulation policy rule files for import into OLE

This repository contains files representing the University of Maryland library circulation policies for use with Kuali OLE.

These files are imported into OLE using the "KRMS Builder" link in the "KRMS Admin" section of the "Admin" tab.

##Helpful Resources

 * Kuali wiki - https://wiki.kuali.org/display/OLE/Circulation+policies
 * Kuali OLE v1.5.6.1 Default Circulation Policy File - https://svn.kuali.org/repos/ole/tags/ole-1.5.6.1/ole-app/olefs/src/main/resources/org/kuali/ole/deliver/defaultload/DefaultCircPolicies.xml
 * Kuali Rice v2.3.6 KRMS Guide - http://site.kuali.org/rice/2.3.6/reference/html/KRMS_Guide.html 
 * Kuali Rice v2.3.6 Documentation Portal - http://site.kuali.org/rice/2.3.6/reference/html/index.html

## File Organization

This repository contains the following files, each corresponding to a KRMS "agenda". This files can be imported into OLE individually.

| Filename  | Notes |
| --------  |------ |
| general_checks.xml | The "General Checks" agenda |
| checkout.xml  | The "Checkout" agenda, handling loan periods |
| checkin.xml | The "Checkin" agenda, handling returns |

## OLE Setup

The following permissions must be added to OLE, in order for certain overrides to function:

| Template Namespace | Template Name | Permission Namespace | Permission Name | Granted to Roles |
| ------------------ | ------------- | -------------------- | --------------- | ---------------- |
| KUALI | Default | OLE-DLVR | Item does not circulate | OLE-PTRN Super Circulation Supervisor |

## License

These files are provided under the CC0 1.0 Universal license (http://creativecommons.org/publicdomain/zero/1.0/).