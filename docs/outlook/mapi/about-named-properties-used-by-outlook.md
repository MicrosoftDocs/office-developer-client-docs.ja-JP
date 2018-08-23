---
title: "Outlook �Ŏg�p���閼�O�t���̃v���p�e�B�ɂ\x82���"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8c245ec2-bb18-ecf0-b4ad-8c164c5924cf
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: 75a08db313ac1b38a400fb329eefa914858ec71e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799600"
---
# <a name="about-named-properties-used-by-outlook"></a><span data-ttu-id="cbef2-103">Outlook �Ŏg�p���閼�O�t���̃v���p�e�B�ɂ���</span><span class="sxs-lookup"><span data-stu-id="cbef2-103">About Named Properties Used by Outlook</span></span>

  
  
<span data-ttu-id="cbef2-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cbef2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cbef2-p101">MAPI �ł́A����̃v���p�e�B�ɖ��O����蓖�Ă�A�ŗL�̎��ʎq����̖��O��}�b�s���O���邽�߁A�Z�b�V�����̊Ԃŉi���I�Ȃ��̖��O�̎��ʎq�̃}�b�s���O��쐬���邽�߂̋@�\��񋟂��܂��B���O�t���v���p�e�B�́A���O�ƃv���p�e�B�̐ݒ�̃O���[�o���Ɉ�ӂ̎��ʎq (GUID) �ɂ���Ď��ʂ��܂��B���O�ɂ́A���l�܂��͕����񂪂ł��܂��BMicrosoft Outlook 2013�܂���Microsoft Outlook 2010�v���p�e�B�̐ݒ��Outlook 2013�܂���Outlook 2010�A **PSETID_Appointment** �Ȃǂɂ���Ē�\`���ꂽ���O��Ԃł͑����̏ꍇ�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-p101">MAPI provides a facility for assigning names to certain properties, for mapping these names to unique identifiers, and for making this name-to-identifier mapping persistent across sessions. Named properties are identified by a name and a globally unique identifier (GUID) for a property set. The name can be a number or a string. For Microsoft Outlook 2013 or Microsoft Outlook 2010, the property set is often a namespace defined by Outlook 2013 or Outlook 2010, such as **PSETID_Appointment**.</span></span> 
  
<span data-ttu-id="cbef2-p102">���O�t���̃v���p�e�B�𑀍삷��ɂ́A [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)�֐���[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)�֐���g�p���܂��B���O�� GUID �v���p�e�B�̐ݒ�́A���݂� MAPI �Z�b�V�����͗L���ȃv���p�e�B���ʎq��擾����[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)�֐��ɓn����܂��B���̃v���p�e�B�̎��ʎq���R���s���[�^�[����ʂ̃R���s���[�^�[�ɈقȂ邱�Ƃ��ł��܂��݈̂�ѐ��̂��閼�O�t���̃v���p�e�B�ɃA�N�Z�X������@�ł́A���̖��O�� GUID �v���p�e�B���킩���Ă��܂��B ���ʎq�͈̔͂́A��� 0x8000 �� 0 xfffe �͈́B</span><span class="sxs-lookup"><span data-stu-id="cbef2-p102">Named properties are manipulated by using the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function and the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) function. The name and the property set GUID are passed to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function to obtain a property identifier that is valid for the current MAPI session. Because this property identifier can vary from computer to computer, the only consistent way to access a named property is to know its name and property set GUID. The range for identifiers is always in the 0x8000 and 0xFFFE range.</span></span> 
  
<span data-ttu-id="cbef2-p103">[IMAPIProp: IUnknown](imapipropiunknown.md)�C���^�[�t�F�C�X���������C�ӂ̃I�u�W�F�N�g�́A���O�t���̃v���p�e�B��T�|�[�g�ł��܂��B��̓I�ɂ́AMAPI �T�[�r�X �v���o�C�[�[�܂��� mapi �́A���O�t���̃v���p�e�B�̒l��擾����[IMAPIProp::GetProps](imapiprop-getprops.md)���������K�v������܂��B���� MAPI �v���o�C�](imapiprop-getprops.md)�[��ڋq�Ƌ��L����Ă���f�[�^��j���̃��X�N�̗��R�ɂ��A���O�t��Outlook 2013�܂���Outlook 2010�ɂ���Ďg�p�����v���p�e�B�̐ݒ�̓T�|�[�g����Ă��܂���B</span><span class="sxs-lookup"><span data-stu-id="cbef2-p103">Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties. Specifically, a MAPI service provider or a MAPI client must implement [IMAPIProp::GetProps](imapiprop-getprops.md) to get values of named properties. Setting named properties used by Outlook 2013 or Outlook 2010 is not supported because of the risk of corrupting data that is shared with other MAPI providers or clients.</span></span> 
  
<span data-ttu-id="cbef2-116">Outlook 2013 および Outlook 2010 は、MAPI 名前付きプロパティなど、その機能の多くを実装するために、添付ファイルのセキュリティおよび会議の代替日時を使用します。</span><span class="sxs-lookup"><span data-stu-id="cbef2-116">Outlook 2013 and Outlook 2010 use MAPI named properties to implement many of their features, for example, attachment security and meeting counter-proposals.</span></span> <span data-ttu-id="cbef2-117">この基になるデータでは、上記 2013 の Outlook と Outlook 2010 これらのプロパティの一部として公開、Outlook 2013 と Outlook 2010 のオブジェクト モデル内のアイテムのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="cbef2-117">Above this underlying data, Outlook 2013 and Outlook 2010 expose some of these properties as item properties in their Outlook 2013 and Outlook 2010 object models.</span></span> <span data-ttu-id="cbef2-118">たとえば、オブジェクト モデルでは、 **ContactItem**オブジェクトの**Email1Address**プロパティは、 **PSETID_Address**名前空間の名前付きの[PidLidEmail1EmailAddress の標準的なプロパティ](pidlidemail1emailaddress-canonical-property.md)に対応します。</span><span class="sxs-lookup"><span data-stu-id="cbef2-118">For example, the **Email1Address** property of the **ContactItem** object in the object model corresponds to the named [PidLidEmail1EmailAddress Canonical Property](pidlidemail1emailaddress-canonical-property.md) in the **PSETID_Address** namespace.</span></span> <span data-ttu-id="cbef2-119">ですが、一般的に、互換性とデータの整合性の問題が発生したため Outlook 2013 および Outlook 2010 で使用される MAPI プロパティの多くに公開されていないオブジェクト モデルです。</span><span class="sxs-lookup"><span data-stu-id="cbef2-119">But in general, due to concerns for compatibility and data integrity, many of the MAPI properties that are used by Outlook 2013 and Outlook 2010 are not exposed in the object model.</span></span> 
  
<span data-ttu-id="cbef2-120">���̃Z���Q�Ƃł́A�����̉��ɋL�ڂ���Ă��閼�O�t���̃v���p�e�B�ɂ��Đ�����܂��B</span><span class="sxs-lookup"><span data-stu-id="cbef2-120">This reference describes a number of named properties that are listed below.</span></span>
  
<span data-ttu-id="cbef2-121">**PSETID_Address** ���O��Ԃ̃v���p�e�B�A���̂Ƃ���ł��B</span><span class="sxs-lookup"><span data-stu-id="cbef2-121">Named properties in the **PSETID_Address** namespace are the following:</span></span> 
  
- [<span data-ttu-id="cbef2-122">PidLidEmail1AddressType ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-122">PidLidEmail1AddressType Canonical Property</span></span>](pidlidemail1addresstype-canonical-property.md)
    
- [<span data-ttu-id="cbef2-123">PidLidEmail1EmailAddress ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-123">PidLidEmail1EmailAddress Canonical Property</span></span>](pidlidemail1emailaddress-canonical-property.md)
    
- [<span data-ttu-id="cbef2-124">PidLidEmail1OriginalEntryId ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-124">PidLidEmail1OriginalEntryId Canonical Property</span></span>](pidlidemail1originalentryid-canonical-property.md)
    
- [<span data-ttu-id="cbef2-125">PidLidEmail2AddressType ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-125">PidLidEmail2AddressType Canonical Property</span></span>](pidlidemail2addresstype-canonical-property.md)
    
- [<span data-ttu-id="cbef2-126">PidLidEmail2DisplayName ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-126">PidLidEmail2DisplayName Canonical Property</span></span>](pidlidemail2displayname-canonical-property.md)
    
- [<span data-ttu-id="cbef2-127">PidLidEmail2EmailAddress ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-127">PidLidEmail2EmailAddress Canonical Property</span></span>](pidlidemail2emailaddress-canonical-property.md)
    
- [<span data-ttu-id="cbef2-128">PidLidEmail2OriginalDisplayName ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-128">PidLidEmail2OriginalDisplayName Canonical Property</span></span>](pidlidemail2originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="cbef2-129">PidLidEmail2OriginalEntryId ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-129">PidLidEmail2OriginalEntryId Canonical Property</span></span>](pidlidemail2originalentryid-canonical-property.md)
    
- [<span data-ttu-id="cbef2-130">PidLidEmail3AddressType ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-130">PidLidEmail3AddressType Canonical Property</span></span>](pidlidemail3addresstype-canonical-property.md)
    
- [<span data-ttu-id="cbef2-131">PidLidEmail3DisplayName ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-131">PidLidEmail3DisplayName Canonical Property</span></span>](pidlidemail3displayname-canonical-property.md)
    
- [<span data-ttu-id="cbef2-132">PidLidEmail3EmailAddress ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-132">PidLidEmail3EmailAddress Canonical Property</span></span>](pidlidemail3emailaddress-canonical-property.md)
    
- [<span data-ttu-id="cbef2-133">PidLidEmail3OriginalDisplayName ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-133">PidLidEmail3OriginalDisplayName Canonical Property</span></span>](pidlidemail3originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="cbef2-134">PidLidEmail3OriginalEntryId ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-134">PidLidEmail3OriginalEntryId Canonical Property</span></span>](pidlidemail3originalentryid-canonical-property.md)
    
- [<span data-ttu-id="cbef2-135">PidLidEmail1DisplayName ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-135">PidLidEmail1DisplayName Canonical Property</span></span>](pidlidemail1displayname-canonical-property.md)
    
- [<span data-ttu-id="cbef2-136">PidLidEmail1OriginalDisplayName ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-136">PidLidEmail1OriginalDisplayName Canonical Property</span></span>](pidlidemail1originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="cbef2-137">PidLidFileUnder ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-137">PidLidFileUnder Canonical Property</span></span>](pidlidfileunder-canonical-property.md)
    
- [<span data-ttu-id="cbef2-138">PidLidInstantMessagingAddress ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-138">PidLidInstantMessagingAddress Canonical Property</span></span>](pidlidinstantmessagingaddress-canonical-property.md)
    
- [<span data-ttu-id="cbef2-139">PidLidWorkAddressCity ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-139">PidLidWorkAddressCity Canonical Property</span></span>](pidlidworkaddresscity-canonical-property.md)
    
- [<span data-ttu-id="cbef2-140">PidLidWorkAddressCountry ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-140">PidLidWorkAddressCountry Canonical Property</span></span>](pidlidworkaddresscountry-canonical-property.md)
    
- [<span data-ttu-id="cbef2-141">PidLidWorkAddressPostalCode ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-141">PidLidWorkAddressPostalCode Canonical Property</span></span>](pidlidworkaddresspostalcode-canonical-property.md)
    
- [<span data-ttu-id="cbef2-142">PidLidWorkAddressPostOfficeBox ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-142">PidLidWorkAddressPostOfficeBox Canonical Property</span></span>](pidlidworkaddresspostofficebox-canonical-property.md)
    
- [<span data-ttu-id="cbef2-143">PidLidWorkAddressState ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-143">PidLidWorkAddressState Canonical Property</span></span>](pidlidworkaddressstate-canonical-property.md)
    
- [<span data-ttu-id="cbef2-144">PidLidWorkAddressStreet ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-144">PidLidWorkAddressStreet Canonical Property</span></span>](pidlidworkaddressstreet-canonical-property.md)
    
- [<span data-ttu-id="cbef2-145">PidLidYomiCompanyName ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-145">PidLidYomiCompanyName Canonical Property</span></span>](pidlidyomicompanyname-canonical-property.md)
    
- [<span data-ttu-id="cbef2-146">PidLidYomiFirstName ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-146">PidLidYomiFirstName Canonical Property</span></span>](pidlidyomifirstname-canonical-property.md)
    
- [<span data-ttu-id="cbef2-147">PidLidYomiLastName ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-147">PidLidYomiLastName Canonical Property</span></span>](pidlidyomilastname-canonical-property.md)
    
<span data-ttu-id="cbef2-148">**PSETID_Appointment** ���O��Ԃ̃v���p�e�B�A���̂Ƃ���ł��B</span><span class="sxs-lookup"><span data-stu-id="cbef2-148">Named properties in the **PSETID_Appointment** namespace are the following:</span></span> 
  
- [<span data-ttu-id="cbef2-149">PidLidAllAttendeesString ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-149">PidLidAllAttendeesString Canonical Property</span></span>](pidlidallattendeesstring-canonical-property.md)
    
- [<span data-ttu-id="cbef2-150">PidLidAppointmentCounterProposal ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-150">PidLidAppointmentCounterProposal Canonical Property</span></span>](pidlidappointmentcounterproposal-canonical-property.md)
    
- [<span data-ttu-id="cbef2-151">PidLidAppointmentDuration ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-151">PidLidAppointmentDuration Canonical Property</span></span>](pidlidappointmentduration-canonical-property.md)
    
- [<span data-ttu-id="cbef2-152">PidLidAppointmentEndWhole ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-152">PidLidAppointmentEndWhole Canonical Property</span></span>](pidlidappointmentendwhole-canonical-property.md)
    
- [<span data-ttu-id="cbef2-153">PidLidAppointmentStartWhole ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-153">PidLidAppointmentStartWhole Canonical Property</span></span>](pidlidappointmentstartwhole-canonical-property.md)
    
- [<span data-ttu-id="cbef2-154">PidLidBusyStatus ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-154">PidLidBusyStatus Canonical Property</span></span>](pidlidbusystatus-canonical-property.md)
    
- [<span data-ttu-id="cbef2-155">PidLidCcAttendeesString ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-155">PidLidCcAttendeesString Canonical Property</span></span>](pidlidccattendeesstring-canonical-property.md)
    
- [<span data-ttu-id="cbef2-156">PidLidLocation ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-156">PidLidLocation Canonical Property</span></span>](pidlidlocation-canonical-property.md)
    
- [<span data-ttu-id="cbef2-157">PidLidRecurring ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-157">PidLidRecurring Canonical Property</span></span>](pidlidrecurring-canonical-property.md)
    
- [<span data-ttu-id="cbef2-158">PidLidToAttendeesString ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-158">PidLidToAttendeesString Canonical Property</span></span>](pidlidtoattendeesstring-canonical-property.md)
    
<span data-ttu-id="cbef2-159">**PSETID_Common** ���O��Ԃ̃v���p�e�B�A���̂Ƃ���ł��B</span><span class="sxs-lookup"><span data-stu-id="cbef2-159">Named properties in the **PSETID_Common** namespace are the following:</span></span> 
  
- [<span data-ttu-id="cbef2-160">PidLidCommonEnd ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-160">PidLidCommonEnd Canonical Property</span></span>](pidlidcommonend-canonical-property.md)
    
- [<span data-ttu-id="cbef2-161">PidLidCommonStart ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-161">PidLidCommonStart Canonical Property</span></span>](pidlidcommonstart-canonical-property.md)
    
- [<span data-ttu-id="cbef2-162">PidLidCompanies ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-162">PidLidCompanies Canonical Property</span></span>](pidlidcompanies-canonical-property.md)
    
- [<span data-ttu-id="cbef2-163">PidLidContacts ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-163">PidLidContacts Canonical Property</span></span>](pidlidcontacts-canonical-property.md)
    
- [<span data-ttu-id="cbef2-164">PidLidCustomFlag ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-164">PidLidCustomFlag Canonical Property</span></span>](pidlidcustomflag-canonical-property.md)
    
- [<span data-ttu-id="cbef2-165">PidLidFormPropStream ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-165">PidLidFormPropStream Canonical Property</span></span>](pidlidformpropstream-canonical-property.md)
    
- [<span data-ttu-id="cbef2-166">PidLidFormStorage ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-166">PidLidFormStorage Canonical Property</span></span>](pidlidformstorage-canonical-property.md)
    
- [<span data-ttu-id="cbef2-167">PidLidHeaderItem ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-167">PidLidHeaderItem Canonical Property</span></span>](pidlidheaderitem-canonical-property.md)
    
- [<span data-ttu-id="cbef2-168">PidLidPageDirStream ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-168">PidLidPageDirStream Canonical Property</span></span>](pidlidpagedirstream-canonical-property.md)
    
- [<span data-ttu-id="cbef2-169">PidLidPropertyDefinitionStream ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-169">PidLidPropertyDefinitionStream Canonical Property</span></span>](pidlidpropertydefinitionstream-canonical-property.md)
    
- [<span data-ttu-id="cbef2-170">PidLidReminderSet ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-170">PidLidReminderSet Canonical Property</span></span>](pidlidreminderset-canonical-property.md)
    
- [<span data-ttu-id="cbef2-171">PidLidReminderTime ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-171">PidLidReminderTime Canonical Property</span></span>](pidlidremindertime-canonical-property.md)
    
- [<span data-ttu-id="cbef2-172">PidLidFlagRequest ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-172">PidLidFlagRequest Canonical Property</span></span>](pidlidflagrequest-canonical-property.md)
    
- [<span data-ttu-id="cbef2-173">PidLidScriptStream ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-173">PidLidScriptStream Canonical Property</span></span>](pidlidscriptstream-canonical-property.md)
    
- [<span data-ttu-id="cbef2-174">PidLidSmartNoAttach ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-174">PidLidSmartNoAttach Canonical Property</span></span>](pidlidsmartnoattach-canonical-property.md)
    
- [<span data-ttu-id="cbef2-175">PidLidToDoTitle ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-175">PidLidToDoTitle Canonical Property</span></span>](pidlidtodotitle-canonical-property.md)
    
- [<span data-ttu-id="cbef2-176">PidLidUseTnef ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-176">PidLidUseTnef Canonical Property</span></span>](pidlidusetnef-canonical-property.md)
    
<span data-ttu-id="cbef2-177">**PSETID_Meeting** ���O��Ԃ̃v���p�e�B�A���̂Ƃ���ł��B</span><span class="sxs-lookup"><span data-stu-id="cbef2-177">Named properties in the **PSETID_Meeting** namespace are the following:</span></span> 
  
- [<span data-ttu-id="cbef2-178">PidLidMeetingType ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-178">PidLidMeetingType Canonical Property</span></span>](pidlidmeetingtype-canonical-property.md)
    
<span data-ttu-id="cbef2-179">**PSETID_Task** ���O��Ԃ̃v���p�e�B�A���̂Ƃ���ł��B</span><span class="sxs-lookup"><span data-stu-id="cbef2-179">Named properties in the **PSETID_Task** namespace are the following:</span></span> 
  
- [<span data-ttu-id="cbef2-180">PidLidTaskActualEffort ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-180">PidLidTaskActualEffort Canonical Property</span></span>](pidlidtaskactualeffort-canonical-property.md)
    
- [<span data-ttu-id="cbef2-181">PidLidTaskDueDate ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-181">PidLidTaskDueDate Canonical Property</span></span>](pidlidtaskduedate-canonical-property.md)
    
- [<span data-ttu-id="cbef2-182">PidLidTaskEstimatedEffort ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-182">PidLidTaskEstimatedEffort Canonical Property</span></span>](pidlidtaskestimatedeffort-canonical-property.md)
    
- [<span data-ttu-id="cbef2-183">PidLidTaskFRecurring ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-183">PidLidTaskFRecurring Canonical Property</span></span>](pidlidtaskfrecurring-canonical-property.md)
    
- [<span data-ttu-id="cbef2-184">PidLidTaskStartDate ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-184">PidLidTaskStartDate Canonical Property</span></span>](pidlidtaskstartdate-canonical-property.md)
    
- [<span data-ttu-id="cbef2-185">PidLidTaskStatus ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-185">PidLidTaskStatus Canonical Property</span></span>](pidlidtaskstatus-canonical-property.md)
    
<span data-ttu-id="cbef2-186">**PS_INTERNET_HEADERS** ���O��Ԃ̃v���p�e�B�A���̂Ƃ���ł��B</span><span class="sxs-lookup"><span data-stu-id="cbef2-186">Named properties in the **PS_INTERNET_HEADERS** namespace are the following:</span></span> 
  
- [<span data-ttu-id="cbef2-187">PidTagInternetReturnPath ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-187">PidTagInternetReturnPath Canonical Property</span></span>](pidtaginternetreturnpath-canonical-property.md)
    
<span data-ttu-id="cbef2-188">**PSETID_Log** ���O��Ԃ̃v���p�e�B�A���̂Ƃ���ł��B</span><span class="sxs-lookup"><span data-stu-id="cbef2-188">Named properties in the **PSETID_Log** namespace are the following:</span></span> 
  
- [<span data-ttu-id="cbef2-189">PidLidLogDuration ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-189">PidLidLogDuration Canonical Property</span></span>](pidlidlogduration-canonical-property.md)
    
- [<span data-ttu-id="cbef2-190">PidLidLogEnd ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-190">PidLidLogEnd Canonical Property</span></span>](pidlidlogend-canonical-property.md)
    
- [<span data-ttu-id="cbef2-191">PidLidLogStart ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-191">PidLidLogStart Canonical Property</span></span>](pidlidlogstart-canonical-property.md)
    
- [<span data-ttu-id="cbef2-192">PidLidLogType ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-192">PidLidLogType Canonical Property</span></span>](pidlidlogtype-canonical-property.md)
    
<span data-ttu-id="cbef2-193">**PS_PUBLIC_STRINGS** ���O��Ԃ̃v���p�e�B�A���̂Ƃ���ł��B</span><span class="sxs-lookup"><span data-stu-id="cbef2-193">Named properties in the **PS_PUBLIC_STRINGS** namespace are the following:</span></span> 
  
- [<span data-ttu-id="cbef2-194">PidNameKeywords ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-194">PidNameKeywords Canonical Property</span></span>](pidnamekeywords-canonical-property.md)
    
- [<span data-ttu-id="cbef2-195">PidNameExchangeJunkEmailMoveStamp ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbef2-195">PidNameExchangeJunkEmailMoveStamp Canonical Property</span></span>](pidnameexchangejunkemailmovestamp-canonical-property.md)
    
## <a name="see-also"></a><span data-ttu-id="cbef2-196">�֘A����</span><span class="sxs-lookup"><span data-stu-id="cbef2-196">See also</span></span>



[<span data-ttu-id="cbef2-197">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="cbef2-197">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="cbef2-198">Outlook がメッセージのヘッダーのみをダウンロードしたかどうかを判別する</span><span class="sxs-lookup"><span data-stu-id="cbef2-198">Determine if Outlook Downloaded Only the Header of a Message</span></span>](how-to-determine-if-outlook-downloaded-only-the-header-of-a-message.md)
  
[<span data-ttu-id="cbef2-199">連絡先アイテムのメール アドレスを取得する</span><span class="sxs-lookup"><span data-stu-id="cbef2-199">Get the Email Address of a Contact Item</span></span>](how-to-get-the-email-address-of-a-contact-item.md)
  
[<span data-ttu-id="cbef2-200">メッセージと共に保存されているユーザー設定フォーム定義を削除する</span><span class="sxs-lookup"><span data-stu-id="cbef2-200">Remove Custom Form Definition Saved With a Message</span></span>](how-to-remove-custom-form-definition-saved-with-a-message.md)

