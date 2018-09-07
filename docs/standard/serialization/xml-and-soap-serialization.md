---
title: XML 및 SOAP Serialization
ms.date: 03/30/2017
helpviewer_keywords:
- SOAP, XML serialization
- XML serialization, SOAP
- serialization, SOAP
- serialization, about serialization
- XML serialization
- serialization
ms.assetid: 832ac524-21bc-419a-a27b-ca8bfc45840f
ms.openlocfilehash: 366a4a42ff0bf968e51e11a66fa81566a47c86ea
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44075285"
---
# <a name="xml-and-soap-serialization"></a><span data-ttu-id="f266d-102">XML 및 SOAP Serialization</span><span class="sxs-lookup"><span data-stu-id="f266d-102">XML and SOAP Serialization</span></span>

<span data-ttu-id="f266d-103">XML serialization은 개체의 public 필드와 속성 또는 메서드의 매개 변수와 반환 값을 특정 XSD(XML 스키마 정의 언어) 문서와 일치하는 XML 스트림으로 변환(serialize)합니다.</span><span class="sxs-lookup"><span data-stu-id="f266d-103">XML serialization converts (serializes) the public fields and properties of an object, or the parameters and return values of methods, into an XML stream that conforms to a specific XML Schema definition language (XSD) document.</span></span> <span data-ttu-id="f266d-104">XML serialization을 사용하면 저장이나 전송을 위해 직렬 형식(이 경우 XML)으로 변환되는 public 속성 및 필드가 있는 강력한 형식의 클래스가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="f266d-104">XML serialization results in strongly typed classes with public properties and fields that are converted to a serial format (in this case, XML) for storage or transport.</span></span>

<span data-ttu-id="f266d-105">XML은 공개 표준이기 때문에 XML 스트림은 플랫폼에 관계없이 필요에 따라 모든 응용 프로그램에서 처리될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f266d-105">Because XML is an open standard, the XML stream can be processed by any application, as needed, regardless of platform.</span></span> <span data-ttu-id="f266d-106">예를 들어 ASP.NET을 사용하여 만들어진 XML Web services는 <xref:System.Xml.Serialization.XmlSerializer> 클래스를 사용하여 데이터를 인터넷이나 인트라넷을 통해 XML Web services 응용 프로그램 간에 전달하는 XML 스트림을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f266d-106">For example, XML Web services created using ASP.NET use the <xref:System.Xml.Serialization.XmlSerializer> class to create XML streams that pass data between XML Web service applications throughout the Internet or on intranets.</span></span> <span data-ttu-id="f266d-107">이와 반대로 deserialization에서는 이러한 XML 스트림을 받아서 개체를 다시 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f266d-107">Conversely, deserialization takes such an XML stream and reconstructs the object.</span></span>

<span data-ttu-id="f266d-108">XML serialization은 SOAP 사양과 일치하는 XML 스트림으로 개체를 serialize하는 데 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f266d-108">XML serialization can also be used to serialize objects into XML streams that conform to the SOAP specification.</span></span> <span data-ttu-id="f266d-109">SOAP는 특히 XML을 사용하여 프로시저 호출을 전송하기 위해 디자인된 XML 기반 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="f266d-109">SOAP is a protocol based on XML, designed specifically to transport procedure calls using XML.</span></span>

<span data-ttu-id="f266d-110">개체를 serialize하거나 deserialize하려면 <xref:System.Xml.Serialization.XmlSerializer> 클래스를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f266d-110">To serialize or deserialize objects, use the <xref:System.Xml.Serialization.XmlSerializer> class.</span></span> <span data-ttu-id="f266d-111">클래스가 serialize되도록 하려면 XML 스키마 정의 도구를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f266d-111">To create the classes to be serialized, use the XML Schema Definition tool.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f266d-112">섹션 내용</span><span class="sxs-lookup"><span data-stu-id="f266d-112">In This Section</span></span>

[<span data-ttu-id="f266d-113">XML serialization 소개</span><span class="sxs-lookup"><span data-stu-id="f266d-113">Introducing XML Serialization</span></span>](introducing-xml-serialization.md)  
<span data-ttu-id="f266d-114">serialization, 특히 XML serialization에 대한 일반 정의를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="f266d-114">Provides a general definition of serialization, particularly XML serialization.</span></span>

[<span data-ttu-id="f266d-115">방법: 개체 직렬화</span><span class="sxs-lookup"><span data-stu-id="f266d-115">How to: Serialize an Object</span></span>](how-to-serialize-an-object.md)  
<span data-ttu-id="f266d-116">개체를 serialize하는 방법을 단계별로 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="f266d-116">Provides step-by-step instructions for serializing an object.</span></span>

[<span data-ttu-id="f266d-117">방법: 개체 deserialize</span><span class="sxs-lookup"><span data-stu-id="f266d-117">How to: Deserialize an Object</span></span>](how-to-deserialize-an-object.md)  
<span data-ttu-id="f266d-118">개체를 deserialize하는 방법을 단계별로 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="f266d-118">Provides step-by-step instructions for deserializing an object.</span></span>

[<span data-ttu-id="f266d-119">XML serialization 예제</span><span class="sxs-lookup"><span data-stu-id="f266d-119">Examples of XML Serialization</span></span>](examples-of-xml-serialization.md)  
<span data-ttu-id="f266d-120">XML serialization의 기본 사항을 보여 주는 예제를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="f266d-120">Provides examples that demonstrate the basics of XML serialization.</span></span>

[<span data-ttu-id="f266d-121">XML 스키마 정의 도구 및 XML serialization</span><span class="sxs-lookup"><span data-stu-id="f266d-121">The XML Schema Definition Tool and XML Serialization</span></span>](the-xml-schema-definition-tool-and-xml-serialization.md)  
<span data-ttu-id="f266d-122">XML 스키마 정의 도구를 사용하여 특정 XSD(XML 스키마 정의 언어) 스키마를 준수하거나 .dll 파일에서 XML 스키마를 생성하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="f266d-122">Describes how to use the XML Schema Definition tool to create classes that adhere to a particular XML Schema definition language (XSD) schema, or to generate an XML Schema from a .dll file.</span></span>

[<span data-ttu-id="f266d-123">특성을 사용하여 XML serialization 제어</span><span class="sxs-lookup"><span data-stu-id="f266d-123">Controlling XML Serialization Using Attributes</span></span>](controlling-xml-serialization-using-attributes.md)  
<span data-ttu-id="f266d-124">특성을 사용하여 serialization을 제어하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="f266d-124">Describes how to control serialization by using attributes.</span></span>

[<span data-ttu-id="f266d-125">XML serialization을 제어하는 특성</span><span class="sxs-lookup"><span data-stu-id="f266d-125">Attributes That Control XML Serialization</span></span>](attributes-that-control-xml-serialization.md)  
<span data-ttu-id="f266d-126">XML serialization의 제어에 사용되는 특성을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="f266d-126">Lists the attributes that are used to control XML serialization.</span></span>

[<span data-ttu-id="f266d-127">방법: XML 스트림의 대체 요소 이름 지정</span><span class="sxs-lookup"><span data-stu-id="f266d-127">How to: Specify an Alternate Element Name for an XML Stream</span></span>](how-to-specify-an-alternate-element-name-for-an-xml-stream.md)  
<span data-ttu-id="f266d-128">serialization을 재정의하여 여러 XML 스트림을 생성하는 방법을 보여 주는 고급 시나리오를 소개합니다.</span><span class="sxs-lookup"><span data-stu-id="f266d-128">Presents an advanced scenario showing how to generate multiple XML streams by overriding the serialization.</span></span>

[<span data-ttu-id="f266d-129">방법: 파생 클래스의 serialization 제어</span><span class="sxs-lookup"><span data-stu-id="f266d-129">How to: Control Serialization of Derived Classes</span></span>](how-to-control-serialization-of-derived-classes.md)  
<span data-ttu-id="f266d-130">파생 클래스의 serialization을 제어하는 방법을 보여 주는 예제를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="f266d-130">Provides an example of how to control the serialization of derived classes.</span></span>

[<span data-ttu-id="f266d-131">방법: XML 요소 및 XML 특성 이름 한정</span><span class="sxs-lookup"><span data-stu-id="f266d-131">How to: Qualify XML Element and XML Attribute Names</span></span>](how-to-qualify-xml-element-and-xml-attribute-names.md)  
<span data-ttu-id="f266d-132">XML 네임스페이스가 XML 스트림에 사용되는 방법을 정의하고 제어하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="f266d-132">Describes how to define and control the way in which XML namespaces are used in the XML stream.</span></span>

[<span data-ttu-id="f266d-133">XML Web Services의 XML serialization</span><span class="sxs-lookup"><span data-stu-id="f266d-133">XML Serialization with XML Web Services</span></span>](xml-serialization-with-xml-web-services.md)  
<span data-ttu-id="f266d-134">XML serialization이 XML Web services에 사용되는 방식을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="f266d-134">Explains how XML serialization is used in XML Web services.</span></span>

[<span data-ttu-id="f266d-135">방법: 개체를 SOAP 인코딩된 XML 스트림으로 직렬화</span><span class="sxs-lookup"><span data-stu-id="f266d-135">How to: Serialize an Object as a SOAP-Encoded XML Stream</span></span>](how-to-serialize-an-object-as-a-soap-encoded-xml-stream.md)  
<span data-ttu-id="f266d-136">사용 하는 방법에 설명 합니다 <xref:System.Xml.Serialization.XmlSerializer> World Wide Web Consortium (W3C) 문서의 5 단원을 준수 하는 인코딩된 SOAP XML 스트림을 만들 클래스 [단순 개체 액세스 프로토콜 (SOAP) 1.1](https://www.w3.org/TR/2000/NOTE-SOAP-20000508/)합니다.</span><span class="sxs-lookup"><span data-stu-id="f266d-136">Describes how to use the <xref:System.Xml.Serialization.XmlSerializer> class to create encoded SOAP XML streams that conform to section 5 of the World Wide Web Consortium (W3C) document titled [Simple Object Access Protocol (SOAP) 1.1](https://www.w3.org/TR/2000/NOTE-SOAP-20000508/).</span></span>

[<span data-ttu-id="f266d-137">방법: 인코딩된 SOAP XML serialization 재정의</span><span class="sxs-lookup"><span data-stu-id="f266d-137">How to: Override Encoded SOAP XML Serialization</span></span>](how-to-override-encoded-soap-xml-serialization.md)  
<span data-ttu-id="f266d-138">개체의 XML serialization을 SOAP 메시지로 재정의하는 프로세스를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="f266d-138">Describes the process for overriding XML serialization of objects as SOAP messages.</span></span>

[<span data-ttu-id="f266d-139">인코딩된 SOAP serialization을 제어하는 특성</span><span class="sxs-lookup"><span data-stu-id="f266d-139">Attributes That Control Encoded SOAP Serialization</span></span>](attributes-that-control-encoded-soap-serialization.md)  
<span data-ttu-id="f266d-140">SOAP로 인코딩된 serialization의 제어에 사용되는 특성을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="f266d-140">Lists the attributes that are used to control SOAP-encoded serialization.</span></span>

[<span data-ttu-id="f266d-141">\<system.xml.serialization> 요소</span><span class="sxs-lookup"><span data-stu-id="f266d-141">\<system.xml.serialization> Element</span></span>](system-xml-serialization-element.md)  
<span data-ttu-id="f266d-142">XML serialization을 제어하기 위한 최상위 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="f266d-142">The top-level configuration element for controlling XML serialization.</span></span>

[<span data-ttu-id="f266d-143">\<dateTimeSerialization> 요소</span><span class="sxs-lookup"><span data-stu-id="f266d-143">\<dateTimeSerialization> Element</span></span>](datetimeserialization-element.md)  
<span data-ttu-id="f266d-144"><xref:System.DateTime> 개체의 serialization 모드를 제어합니다.</span><span class="sxs-lookup"><span data-stu-id="f266d-144">Controls the serialization mode of <xref:System.DateTime> objects.</span></span>

[<span data-ttu-id="f266d-145">\<schemaImporterExtensions> 요소</span><span class="sxs-lookup"><span data-stu-id="f266d-145">\<schemaImporterExtensions> Element</span></span>](schemaimporterextensions-element.md)  
<span data-ttu-id="f266d-146"><xref:System.Xml.Serialization.XmlSchemaImporter> 클래스에서 사용하는 형식을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="f266d-146">Contains types that are used by the <xref:System.Xml.Serialization.XmlSchemaImporter> class.</span></span>

[<span data-ttu-id="f266d-147">\<추가 > 요소에 대 한 \<schemaImporterExtensions ></span><span class="sxs-lookup"><span data-stu-id="f266d-147">\<add> Element for \<schemaImporterExtensions></span></span>](add-element-for-schemaimporterextensions.md)  
<span data-ttu-id="f266d-148"><xref:System.Xml.Serialization.XmlSchemaImporter> 클래스에서 사용하는 형식을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f266d-148">Adds types that are used by the <xref:System.Xml.Serialization.XmlSchemaImporter> class.</span></span>

## <a name="related-sections"></a><span data-ttu-id="f266d-149">관련 단원</span><span class="sxs-lookup"><span data-stu-id="f266d-149">Related Sections</span></span>

[<span data-ttu-id="f266d-150">고급 개발 기술</span><span class="sxs-lookup"><span data-stu-id="f266d-150">Advanced Development Technologies</span></span>](https://msdn.microsoft.com/library/c4a7e341-f0c6-4df4-a74f-223387ac6e4e)  
<span data-ttu-id="f266d-151">.NET Framework의 복잡한 개발 작업 및 기술에 대한 자세한 내용을 볼 수 있는 링크를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="f266d-151">Provides links to more information on sophisticated development tasks and techniques in the .NET Framework.</span></span>

[<span data-ttu-id="f266d-152">ASP.NET 및 XML Web Service 클라이언트를 사용하여 만든 XML Web Services</span><span class="sxs-lookup"><span data-stu-id="f266d-152">XML Web Services Created Using ASP.NET and XML Web Service Clients</span></span>](https://msdn.microsoft.com/library/1e64af78-d705-4384-b08d-591a45f4379c)  
<span data-ttu-id="f266d-153">ASP.NET을 사용하여 XML Web services를 프로그래밍하는 방법을 설명하는 항목을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="f266d-153">Provides topics that describe and explain how to program XML Web services using ASP.NET.</span></span>

## <a name="see-also"></a><span data-ttu-id="f266d-154">참고자료</span><span class="sxs-lookup"><span data-stu-id="f266d-154">See also</span></span>

- [<span data-ttu-id="f266d-155">이진 serialization</span><span class="sxs-lookup"><span data-stu-id="f266d-155">Binary Serialization</span></span>](binary-serialization.md)
