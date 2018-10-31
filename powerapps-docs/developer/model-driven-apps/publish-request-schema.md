---
title: "Publish request schema  (model-driven apps) | Microsoft Docs" # Intent and product brand in a unique string of 43-59 chars including spaces
description: "The following is the schema definition for the PublishXmlRequest message." # 115-145 characters including spaces. This abstract displays in the search result.
ms.custom: ""
ms.date: 10/31/2018
ms.reviewer: ""
ms.service: "powerapps"
ms.topic: "article"
author: "KumarVivek" # GitHub ID
ms.author: "kvivek" # MSFT alias of Microsoft employees only
manager: "shilpas" # MSFT alias of manager or PM counterpart
---
# Publish request schema

<!-- https://docs.microsoft.com/en-us/dynamics365/customer-engagement/developer/customize-dev/publish-request-schema -->

The following is the schema definition for the <xref:Microsoft.Crm.Sdk.Messages.PublishXmlRequest> message. For more information, see [Publish Customizations](publish-customizations.md). [!INCLUDE[schema_download](../../includes/schema-download.md)].  
  
## Schema  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<xs:schema attributeFormDefault="unqualified"  
           elementFormDefault="qualified"  
           xmlns:xs="http://www.w3.org/2001/XMLSchema">  
 <xs:element name="importexportxml">  
  <xs:complexType>  
   <xs:sequence>  
    <xs:element name="entities"  
                minOccurs="0">  
     <xs:complexType>  
      <xs:sequence minOccurs="0"  
                   maxOccurs="unbounded">  
       <!-- Name of the entity to publish-->  
       <xs:element maxOccurs="unbounded"  
                   name="entity"  
                   type="xs:string" />  
      </xs:sequence>  
     </xs:complexType>  
    </xs:element>  
    <xs:element name="ribbons"  
                minOccurs="0">  
     <xs:complexType>  
      <xs:sequence minOccurs="0"  
                   maxOccurs="unbounded">  
       <!-- Application ribbon. : This value is not used. We publish the application ribbon if there is at least one <ribbon> node present -->  
       <xs:element maxOccurs="unbounded"  
                   name="ribbon"  
                   type="xs:string" />  
      </xs:sequence>  
     </xs:complexType>  
    </xs:element>  
    <xs:element name="dashboards"  
                minOccurs="0">  
     <xs:complexType>  
      <xs:sequence minOccurs="0"  
                   maxOccurs="unbounded">  
       <!-- Guid of the systemform to publish-->  
       <xs:element maxOccurs="unbounded"  
                   name="dashboard"  
                   type="xs:string" />  
      </xs:sequence>  
     </xs:complexType>  
    </xs:element>  
    <xs:element name="optionsets"  
                minOccurs="0">  
     <xs:complexType>  
      <xs:sequence minOccurs="0"  
                   maxOccurs="unbounded">  
       <!-- Name of the optionset to publish-->  
       <xs:element maxOccurs="unbounded"  
                   name="optionset"  
                   type="xs:string" />  
      </xs:sequence>  
     </xs:complexType>  
    </xs:element>  
    <xs:element name="sitemaps"  
                minOccurs="0">  
     <xs:complexType>  
      <xs:sequence minOccurs="0"  
                   maxOccurs="unbounded">  
       <!-- Guid of the sitemap to publish : This value is not used. We publish the sitemap if there is at least one <sitemap> node present-->  
       <xs:element maxOccurs="unbounded"  
                   name="sitemap"  
                   type="xs:string" />  
      </xs:sequence>  
     </xs:complexType>  
    </xs:element>  
    <xs:element name="webresources"  
                minOccurs="0">  
     <xs:complexType>  
      <xs:sequence minOccurs="0"  
                   maxOccurs="unbounded">  
       <!-- Guid of the web resource to publish -->  
       <xs:element maxOccurs="unbounded"  
                   name="webresource"  
                   type="xs:string" />  
      </xs:sequence>  
     </xs:complexType>  
    </xs:element>  
   </xs:sequence>  
  </xs:complexType>  
 </xs:element>  
</xs:schema>  
  
```  
  
### See also  
 <xref:Microsoft.Crm.Sdk.Messages.PublishXmlRequest>   
 [Publish Customizations](publish-customizations.md)   
 [Schemas used in Model-driven apps](/dynamics365/customer-engagement/developer/schemas-used-dynamics-365)