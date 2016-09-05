---
title: Thumbnail service
labels:
    - thumbnail
    - 5-7-1
toc: true
confluence:
    ajs-parent-page-id: '17334368'
    ajs-parent-page-title: Other services
    ajs-space-key: NXDOC58
    ajs-space-name: 'Nuxeo Platform Developer Documentation - 5.8 '
    canonical: Thumbnail+service
    canonical_source: 'https://doc.nuxeo.com/display/NXDOC58/Thumbnail+service'
    page_id: '17334502'
    shortlink: 5oAIAQ
    shortlink_source: 'https://doc.nuxeo.com/x/5oAIAQ'
    source_link: /display/NXDOC58/Thumbnail+service
history:
    - 
        author: Solen Guitter
        date: '2013-11-15 11:46'
        message: eplaced afterBlobUpdateCheck event by scheduleThumbnailUpdat
        version: '28'
    - 
        author: Solen Guitter
        date: '2013-11-13 12:17'
        message: Updated links to 5.8 release
        version: '27'
    - 
        author: Solen Guitter
        date: '2013-09-05 15:51'
        message: ''
        version: '26'
    - 
        author: Solen Guitter
        date: '2013-09-04 16:43'
        message: ''
        version: '25'
    - 
        author: Vladimir Pasquier
        date: '2013-07-22 14:21'
        message: ''
        version: '24'
    - 
        author: Solen Guitter
        date: '2013-06-28 14:10'
        message: Fixed format
        version: '23'
    - 
        author: Vladimir Pasquier
        date: '2013-06-20 15:55'
        message: ''
        version: '22'
    - 
        author: Vladimir Pasquier
        date: '2013-06-20 11:08'
        message: ''
        version: '21'
    - 
        author: Vladimir Pasquier
        date: '2013-06-20 11:04'
        message: ''
        version: '20'
    - 
        author: Vladimir Pasquier
        date: '2013-06-20 10:58'
        message: ''
        version: '19'
    - 
        author: Vladimir Pasquier
        date: '2013-06-20 10:58'
        message: ''
        version: '18'
    - 
        author: Vladimir Pasquier
        date: '2013-06-20 10:34'
        message: ''
        version: '17'
    - 
        author: Vladimir Pasquier
        date: '2013-06-19 15:56'
        message: ''
        version: '16'
    - 
        author: Vladimir Pasquier
        date: '2013-06-18 18:37'
        message: ''
        version: '15'
    - 
        author: Vladimir Pasquier
        date: '2013-06-18 18:25'
        message: ''
        version: '14'
    - 
        author: Vladimir Pasquier
        date: '2013-06-18 17:56'
        message: ''
        version: '13'
    - 
        author: Vladimir Pasquier
        date: '2013-06-18 17:53'
        message: ''
        version: '12'
    - 
        author: Vladimir Pasquier
        date: '2013-06-18 15:50'
        message: ''
        version: '11'
    - 
        author: Vladimir Pasquier
        date: '2013-06-18 15:48'
        message: ''
        version: '10'
    - 
        author: Vladimir Pasquier
        date: '2013-06-18 15:48'
        message: ''
        version: '9'
    - 
        author: Vladimir Pasquier
        date: '2013-06-18 15:48'
        message: ''
        version: '8'
    - 
        author: Vladimir Pasquier
        date: '2013-06-18 15:46'
        message: ''
        version: '7'
    - 
        author: Vladimir Pasquier
        date: '2013-06-18 15:46'
        message: ''
        version: '6'
    - 
        author: Vladimir Pasquier
        date: '2013-06-18 15:23'
        message: ''
        version: '5'
    - 
        author: Vladimir Pasquier
        date: '2013-06-18 15:22'
        message: ''
        version: '4'
    - 
        author: Vladimir Pasquier
        date: '2013-06-18 12:38'
        message: ''
        version: '3'
    - 
        author: Vladimir Pasquier
        date: '2013-06-18 11:09'
        message: ''
        version: '2'
    - 
        author: Vladimir Pasquier
        date: '2013-06-18 10:24'
        message: ''
        version: '1'

---
Here are the different components of the thumbnail feature:

*   **Thumbnail service**
    The service that handles thumbnail factories contributions.
*   Interface: `[ThumbnailService](http://community.nuxeo.com/api/nuxeo/5.7/javadoc/org/nuxeo/ecm/core/api/thumbnail/ThumbnailService.html),
    `
*   Implementation: `[ThumbnailServiceImpl](http://community.nuxeo.com/api/nuxeo/5.8/javadoc/org/nuxeo/ecm/core/api/thumbnail/ThumbnailServiceImpl.html),
    `
*   <span class="componentTitle">Component:</span> `[<span class="componentTitle">org.nuxeo.ecm.core.api.thumbnail.ThumbnailService</span>](http://explorer.nuxeo.org/nuxeo/site/distribution/Nuxeo Platform-5.8/viewComponent/org.nuxeo.ecm.core.api.thumbnail.ThumbnailService),
    `
*   Extension point: `[thumbnailFactory](http://explorer.nuxeo.org/nuxeo/site/distribution/Nuxeo Platform-5.8/viewExtensionPoint/org.nuxeo.ecm.core.api.thumbnail.ThumbnailService--thumbnailFactory).
    `

*   **Default Thumbnail factories**

    *   [`ThumbnailDocumentFactory`](http://community.nuxeo.com/api/nuxeo/5.8/javadoc/org/nuxeo/ecm/platform/thumbnail/factories/ThumbnailDocumentFactory.html): Default thumbnail factory for all non-folderish documents. Returns the main blob converted in thumbnail or get the document's big icon as a thumbnail.
    *   [`ThumbnailFolderishFactory`](http://community.nuxeo.com/api/nuxeo/5.8/javadoc/org/nuxeo/ecm/platform/thumbnail/factories/ThumbnailFolderishFactory.html): Default thumbnail factory for all folderish documents.
    *   [`ThumbnailPictureFactory`](http://community.nuxeo.com/api/nuxeo/5.8/javadoc/org/nuxeo/ecm/platform/picture/thumbnail/ThumbnailPictureFactory.html): Default Picture thumbnail factory.
    *   [`ThumbnailVideoFactory`](http://community.nuxeo.com/api/nuxeo/5.8/javadoc/org/nuxeo/ecm/platform/video/adapter/ThumbnailVideoFactory.html): Video thumbnail factory from [DAM]({{page page='digital-asset-management-dam'}}).
    *   [`ThumbnailAudioFactory`](http://community.nuxeo.com/api/nuxeo/5.8/javadoc/org/nuxeo/ecm/platform/audio/extension/ThumbnailAudioFactory.html): Audio thumbnail factory from [DAM]({{page page='digital-asset-management-dam'}}).

*   **Thumbnail listeners**

    *   [`UpdateThumbnailListener`](http://community.nuxeo.com/api/nuxeo/5.8/javadoc/org/nuxeo/ecm/platform/thumbnail/listener/UpdateThumbnailListener.html): Thumbnail listener handling creation and update of document event to store document thumbnail preview (only for the File document type).
    *   [`CheckBlobUpdateListener`](http://community.nuxeo.com/api/nuxeo/5.8/javadoc/org/nuxeo/ecm/platform/thumbnail/listener/CheckBlobUpdateListener.html): Thumbnail listener handling document blob update and checking changes. Fires a [`scheduleThumbnailUpdate`](http://community.nuxeo.com/api/nuxeo/5.8/javadoc/org/nuxeo/ecm/platform/thumbnail/ThumbnailConstants.EventNames.html#scheduleThumbnailUpdate) event if it's the case that will trigger [`UpdateThumbnailListener`](http://community.nuxeo.com/api/nuxeo/5.8/javadoc/org/nuxeo/ecm/platform/thumbnail/listener/UpdateThumbnailListener.html).

{{#> callout type='info' heading='Thumbnail factory on GitHub'}}

<span style="color: rgb(0,0,0);">Here are Nuxeo thumbnail factory implementations on GitHub:
</span>

*   `[ThumbnailDocumentFactory](https://github.com/nuxeo/nuxeo-features/blob/release-5.8/nuxeo-thumbnail/src/main/java/org/nuxeo/ecm/platform/thumbnail/factories/ThumbnailDocumentFactory.java),
    `
*   `[ThumbnailVideoFactory](https://github.com/nuxeo/nuxeo-platform-video/blob/release-5.8/nuxeo-platform-video-core/src/main/java/org/nuxeo/ecm/platform/video/adapter/ThumbnailVideoFactory.java),
    `
*   `[ThumbnailAudioFactory](https://github.com/nuxeo/nuxeo-platform-audio/blob/release-5.8/nuxeo-platform-audio-core/src/main/java/org/nuxeo/ecm/platform/audio/extension/ThumbnailAudioFactory.java),
    `
*   `[ThumbnailPictureFactory](https://github.com/nuxeo/nuxeo-features/blob/release-5.8/nuxeo-platform-imaging/nuxeo-platform-imaging-core/src/main/java/org/nuxeo/ecm/platform/picture/thumbnail/ThumbnailPictureFactory.java).
    `

{{/callout}}

## Registering a New Thumbnail Factory

A thumbnail factory can be registered using the following example extension:

```html/xml
<extension target="org.nuxeo.ecm.core.api.thumbnail.ThumbnailService"
    point="thumbnailFactory">

    <thumbnailFactory name="thumbnailFolderishFactory" facet="Folderish"
      factoryClass="org.nuxeo.ecm.platform.thumbnail.factories.ThumbnailFolderishFactory" />

    <thumbnailFactory name="thumbnailAudioFactory" docType="Audio"
      factoryClass="org.nuxeo.ecm.platform.audio.extension.ThumbnailAudioFactory" />

 </extension>

```

The above thumbnail factories will be used to compute and fetch specific thumbnails for folderish documents on one hand, and audio documents on the other hand. Here are their properties:

*   `docType`: string identifying the related document type. In the example, the type is "Audio".
*   `facet`: string identifying the related document facet. In the example, the facet is "Folderish".
*   `factoryClass`: string representing the class name of the factory to use.

Each factory should implement the interface [`ThumbnailFactory`](http://community.nuxeo.com/api/nuxeo/5.8/javadoc/org/nuxeo/ecm/core/api/thumbnail/class-use/ThumbnailFactory.html). This interface contract contains two methods to implement:

*   `Blob getThumbnail(DocumentModel doc, CoreSession session)`: gets the document thumbnail (related to the doc type/facet).
*   `Blob computeThumbnail(DocumentModel doc, CoreSession session)`: computes the thumbnail (related to the document type/facet).

The listener [`UpdateThumbnailListener`](http://community.nuxeo.com/api/nuxeo/5.8/javadoc/org/nuxeo/ecm/platform/thumbnail/listener/UpdateThumbnailListener.html) is calling `YourFactory#computeThumbnail` that allows developers to compute the document blob when creating a document and after updating it (if the blob related to this document has been changed).

&nbsp;When computing your thumbnail, [`UpdateThumbnailListener`](http://community.nuxeo.com/api/nuxeo/5.8/javadoc/org/nuxeo/ecm/platform/thumbnail/listener/UpdateThumbnailListener.html) stores it into a specific metadata&nbsp; <span style="color: rgb(51,51,51);">`<span style="color: rgb(51,51,51);">thumb:thumbnail</span>` provided by the following schema:</span>

```html/xml
  <xs:schema xmlns:nxs="http://www.nuxeo.org/ecm/schemas/thumbnail"
  xmlns:xs="http://www.w3.org/2001/XMLSchema" targetNamespace="http://www.nuxeo.org/ecm/schemas/thumbnail">

  <xs:include schemaLocation="core-types.xsd" />

  <xs:element name="thumbnail" type="nxs:content" />

  </xs:schema>

```

This process can be useful to avoid lazy loading when displaying documents list.

## Picture Thumbnail Example

Here is an example with the picture thumbnail factory, which is fetching a image existing into the picture schema.

```java
import org.nuxeo.common.utils.FileUtils;
import org.nuxeo.ecm.core.api.Blob;
import org.nuxeo.ecm.core.api.CoreSession;
import org.nuxeo.ecm.core.api.DocumentModel;
import org.nuxeo.ecm.core.api.impl.blob.FileBlob;
import org.nuxeo.ecm.platform.picture.api.PictureView;
import org.nuxeo.ecm.platform.picture.api.adapters.MultiviewPicture;
import org.nuxeo.ecm.platform.types.adapter.TypeInfo;

public class ThumbnailPictureFactory implements ThumbnailFactory {
    @Override
    public Blob getThumbnail(DocumentModel doc, CoreSession session)
            throws ClientException {
        if (!doc.hasFacet("Picture")) {
            throw new ClientException("Document is not a picture");
        }
        // Choose the nuxeo default thumbnail of the picture views if exists
        MultiviewPicture mViewPicture = doc.getAdapter(MultiviewPicture.class);
        PictureView thumbnailView = mViewPicture.getView("Small");
        if (thumbnailView == null || thumbnailView.getBlob() == null) {
            // try thumbnail view
            thumbnailView = mViewPicture.getView("Thumbnail");
            if (thumbnailView == null || thumbnailView.getBlob() == null) {
                TypeInfo docType = doc.getAdapter(TypeInfo.class);
                return new FileBlob(
                        FileUtils.getResourceFileFromContext("nuxeo.war"
                                + File.separator + docType.getBigIcon()));
            }
        }
        return thumbnailView.getBlob();
    }
    @Override
    public Blob computeThumbnail(DocumentModel doc, CoreSession session) {
        return null;
    }
}

```

And then the usage of `ThumbnailAdapter`:

```java
import org.nuxeo.common.utils.FileUtils;
import org.nuxeo.ecm.core.api.Blob;
import org.nuxeo.ecm.core.api.CoreSession;
import org.nuxeo.ecm.core.api.DocumentModel;
import org.nuxeo.ecm.core.api.blobholder.BlobHolder;
import org.nuxeo.ecm.core.api.impl.DocumentModelImpl;
import org.nuxeo.ecm.core.api.impl.blob.FileBlob;
import org.nuxeo.ecm.core.api.thumbnail.ThumbnailAdapter;
import org.nuxeo.ecm.core.api.CoreSession;
import com.google.inject.Inject;

@Inject
CoreSession session;

// Create a picture
DocumentModel root = session.getRootDocument();
DocumentModel picture = new DocumentModelImpl(root.getPathAsString(),"pic", "Picture");
picture.setPropertyValue("picture:views", (Serializable) createViews());
picture = session.createDocument(picture);
session.save();

// Using BlobHolder adapter
BlobHolder bh = picture.getAdapter(BlobHolder.class);
Blob blob = new FileBlob(getFileFromPath("test-data/big_nuxeo_logo.gif"), "image/gif",null, "big_nuxeo_logo.gif", null);
bh.setBlob(blob);
session.saveDocument(picture);
session.save();

// Using ThumbnailAdapter
ThumbnailAdapter pictureThumbnail = picture.getAdapter(ThumbnailAdapter.class);
Blob thumbnail = pictureThumbnail.getThumbnail(session);
String fileName = thumbnail.getFilename();
```

&nbsp;

Default Nuxeo thumbnail factories fall back on **Nuxeo Document BigIcon** if no thumbnail has been found.

Here is a way to find it properly:

```java
     Blob getDefaultThumbnail(DocumentModel doc) {
        if (doc == null) {
            return null;
        }
        TypeInfo docType = doc.getAdapter(TypeInfo.class);
        String iconPath = docType.getBigIcon();
        if (iconPath == null) {
            iconPath = docType.getIcon();
        }
        if (iconPath == null) {
            return null;
        }
        FacesContext ctx = FacesContext.getCurrentInstance();
        if (ctx == null) {
            return null;
        }
        try {
            InputStream iconStream = ctx.getExternalContext().getResourceAsStream(
                    iconPath);
            if (iconStream != null) {
                return new FileBlob(iconStream);
            }
        } catch (IOException e) {
            log.warn(String.format(
                    "Could not fetch the thumbnail blob from icon path '%s'",
                    iconPath), e);
        }
        return null;
    }

```

## Thumbnail Architecture

Here, we can see the `ThumbnailAdapter` to use and factories like the default one `ThumbnailDocumentFactory` and `ThumbnailPictureFactory`:

![]({{file name='thumbnail.png'}} ?w=650,border=true)_
Powered by [yFiles](http://www.yworks.com)_