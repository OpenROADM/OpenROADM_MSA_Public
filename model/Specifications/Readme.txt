The Json Files of "Specification" Directory can be used to fill the OpenROADM part
of operational modes catalog in the Data Store of the ROADM Network Controller (RNC):

_body-rpc-add-operational-modes-to -catalog-[ORrelease]-optical-spec-[spec-release] 
can be used as the body of the add-openroadm-operational-modes-to-catalog RPC 

_apidoc-operational-modes-catalog-[ORrelease]-optical-spec-[spec-release]
can be used to post the specifications to the operational modes catalog directly 
targeting the catalog in the service Data Store of the RNC. 

After this operation, the operational modes catalog will then contain
the translation of the [spec-release] version of OpenROADM optical specifications.
 
Note : no file is provided to fill the part of the catalog dedicated to specific
operational modes, since associated specifications are not intended to be publicly
released.

__ORrelease 10_1 : first version of the catalog in which Amplifier node is not
correctly structured. To be used when RNC implements Service model 10.0.0/10.1.0

__ORrelease 12_0 : corrects the amplifier yang node structure. To be used when
the RNC implements at least Service model 12.0.0.

__ORrelease 13_1 : Introduce Optical specification version 6. To be used when
the RNC implements at least Service model 12.0.0 and Common models R13.1.0 where
pcs-dp-qam16 enum is introduced to support PCS modulation format.

__ORrelease 15_0 : Uses Optical specification version 6. To be used when the
RNC implements at least Common models R13.1.0 and Service model 15.0.0 where
max-channel-number is introduced in Catalog Add-Blocks parameters to
differentiate MW-WR-Core-type2 from MW-WR-Core. Files (both for apidoc and rpc)
are corrected in R16.0.0, to include min-OOB-osnr-single-channel-value for all
modes (mandatory parameter) and correct fec-type incorrectly filled for some modes.

__ORrelease 16_0 : Uses Optical specification version 6. To be used when the
RNC implements at least Common models R13.1.0 and Service model 16.0.0, where
some transponder parameters have been set to optional in the catalog, to cope
with the evolutions of the specifications that were not correctly captured in
R15.0, and simplify the description of specific-operational-modes (modulation
-format, TX-OOB-single/multi-channel-value).
Introduction of media-interface-id defined by CMIS for OR transponders.

__ORrelease 16_1 : Uses Optical specification version 6. To be used when the
RNC implements at least Common models R16.1.0 and Service model 16.1.0, where
some parameters were added to xponder-pluggables in the catalog:
payload-rate-identity,rw fec-rate, prefec-ber-threshold; and where min/max
central-frequencies were changed to min/max-edge-frequencies in grid-parameters.