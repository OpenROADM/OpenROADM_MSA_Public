The Json Files of "Specification" Directory can be used to fill the OpenROADM part
of operational modes catalog in the Data Store of the ROADM Network Controller (RNC):

_body-rpc-add-operational-modes-to -catalog-[ORrelease]-optical-spec-[spec-release] 
can be used as the body of the add-openroadm-operational-modes-to-catalog RPC 

_apidoc-operational-modes-catalog-[ORrelease]-optical-spec-[spec-release]
can be used to post the specifications to the operational modes catalog directly 
targeting the catalog in the service Data Store of the RNC. 

__ORrelease 10_1 : first version of the catalog in which Amplifier node is not
correctly structured. To be used when RNC implements Service model 10.0.0/10.1.0

__ORrelease 12_0 : corrects the amplifier yang node structure. To be used when
the RNC implements at least Service model 12.0.0.

__ORrelease 13_1 : Introduce Optical specification version 6. To be used when
the RNC implements at least Service model 12.0.0 and Common models R13.1.0 where
pcs-dp-qam16 enum is introduced to support PCS modulation format.
  
After this operation, the operational modes catalog will then contain
the translation of the [spec-release] version of OpenROADM optical specifications.
 
Note : no file is provided to fill the part of the catalog dedicated to specific
operational modes, since associated specifications are not intended to be publicly
released.
