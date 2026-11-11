# OFBiz EDI

A plugin for Apache OFBiz that exchanges EDI documents with trading partners through EDI networks.
SPS Commerce is the first network. TrueCommerce, Orderful and Cleo follow.

EDI is the standard file format companies use to exchange orders and shipping notices. In the USA and Canada it is mostly X12.

## How it works

- A connection holds one network account, with its login encrypted.
- Every file in or out is saved first as an exchange record, with its state, tries and errors. A file seen twice is handled once.
- Files are read into common documents in JSON: order, ship advice, ship notice, expected receipt, receipt advice and acknowledgment.
- Every network follows one shared contract: fetch files, send a file, read a file into a common document, write a common document into a file.
- Maps are templates, with draft, preview, checks, publish and going back.
- It does not change OFBiz core code.

## Install

Clone this repository into the `plugins` folder of an OFBiz trunk checkout:

```
cd ofbiz-framework/plugins
git clone https://github.com/hotwaxsystems/ofbiz-edi.git edi
```

## Contributing

Every change goes through a pull request.

## License

Apache License 2.0. See `LICENSE` and `NOTICE`.
