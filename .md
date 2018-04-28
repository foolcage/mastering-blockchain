## Organization

## peer

## order

## channel

## network

## client(user)
* admin
* user

method:  
principal including(identity properties)

msp:  
membership rules of an organization

## 例子
```
crypto-config
├── ordererOrganizations
│   └── example.com
│       ├── ca
│       │   ├── ca.example.com-cert.pem (2,signed by ca self)
│       │   └── e2b69ae48ff64f3490ec1e606cb861107d21af0c4921a1725df8af8c7936ff95_sk (1,generate ca private key)
│       ├── msp
│       │   ├── admincerts
│       │   │   └── Admin@example.com-cert.pem (21,copy from 17)
│       │   ├── cacerts
│       │   │   └── ca.example.com-cert.pem (5,copy from 2)
│       │   └── tlscacerts
│       │       └── tlsca.example.com-cert.pem (6,copy from 4)
│       ├── orderers
│       │   └── orderer.example.com
│       │       ├── msp
│       │       │   ├── admincerts
│       │       │   │   └── Admin@example.com-cert.pem (22,copy from 17)
│       │       │   ├── cacerts
│       │       │   │   └── ca.example.com-cert.pem (9,copy from 5)
│       │       │   ├── keystore
│       │       │   │   └── 080f8694cb7935215965e967886541b0102e88efc77f3fe4d78e28b25b32bc35_sk (7,generate peer private key)
│       │       │   ├── signcerts
│       │       │   │   └── orderer.example.com-cert.pem (8,signed by 1)
│       │       │   └── tlscacerts
│       │       │       └── tlsca.example.com-cert.pem (10,copy from 6)
│       │       └── tls
│       │           ├── ca.crt (13,copy from 4)
│       │           ├── server.crt (12,sign by 3)
│       │           └── server.key (11,generate private key)
│       ├── tlsca
│       │   ├── dade83e7ac490b35415cd2608675a8f47dcec698159b00933979fd98f90445f1_sk (3,generate tlsca private key)
│       │   └── tlsca.example.com-cert.pem (4,signed by tlsca self)
│       └── users
│           └── Admin@example.com
│               ├── msp
│               │   ├── admincerts
│               │   │   └── Admin@example.com-cert.pem (17,copy from 15)
│               │   ├── cacerts
│               │   │   └── ca.example.com-cert.pem (16,copy from 2)
│               │   ├── keystore
│               │   │   └── 3ed5ea19611209ce9a1ce6313fbb53fe5864076ac3a8a0a9bea9dc6a49e55bf0_sk (14,generate admin private key)
│               │   ├── signcerts
│               │   │   └── Admin@example.com-cert.pem (15,sign by 1)
│               │   └── tlscacerts
│               │       └── tlsca.example.com-cert.pem (copy from 4)
│               └── tls
│                   ├── ca.crt (20,copy from 4)
│                   ├── client.crt (19,signed by 3)
│                   └── client.key (18,generate private key)
└── peerOrganizations
    ├── org1.example.com
    │   ├── ca
    │   │   ├── 99de79d3078f0054159badf4832aed3b13085b9c5ef56efdac0f58c598d7202b_sk
    │   │   └── ca.org1.example.com-cert.pem
    │   ├── msp
    │   │   ├── admincerts
    │   │   │   └── Admin@org1.example.com-cert.pem
    │   │   ├── cacerts
    │   │   │   └── ca.org1.example.com-cert.pem
    │   │   ├── config.yaml
    │   │   └── tlscacerts
    │   │       └── tlsca.org1.example.com-cert.pem
    │   ├── peers
    │   │   ├── peer0.org1.example.com
    │   │   │   ├── msp
    │   │   │   │   ├── admincerts
    │   │   │   │   │   └── Admin@org1.example.com-cert.pem
    │   │   │   │   ├── cacerts
    │   │   │   │   │   └── ca.org1.example.com-cert.pem
    │   │   │   │   ├── config.yaml
    │   │   │   │   ├── keystore
    │   │   │   │   │   └── 862803284d68c2d1b989bbe5c11aad2f41890424bdcdda69501d13e51ade357d_sk
    │   │   │   │   ├── signcerts
    │   │   │   │   │   └── peer0.org1.example.com-cert.pem
    │   │   │   │   └── tlscacerts
    │   │   │   │       └── tlsca.org1.example.com-cert.pem
    │   │   │   └── tls
    │   │   │       ├── ca.crt
    │   │   │       ├── server.crt
    │   │   │       └── server.key
    │   │   └── peer1.org1.example.com
    │   │       ├── msp
    │   │       │   ├── admincerts
    │   │       │   │   └── Admin@org1.example.com-cert.pem
    │   │       │   ├── cacerts
    │   │       │   │   └── ca.org1.example.com-cert.pem
    │   │       │   ├── config.yaml
    │   │       │   ├── keystore
    │   │       │   │   └── 802c3d9e030ac6ac00bf45180ba055b42c8e56a514a323f6e869eeedcd5f47da_sk
    │   │       │   ├── signcerts
    │   │       │   │   └── peer1.org1.example.com-cert.pem
    │   │       │   └── tlscacerts
    │   │       │       └── tlsca.org1.example.com-cert.pem
    │   │       └── tls
    │   │           ├── ca.crt
    │   │           ├── server.crt
    │   │           └── server.key
    │   ├── tlsca
    │   │   ├── 32faaf55e4393d98bb93ea46e1ce706118a7930fba6ca73cb569f735c3133da3_sk
    │   │   └── tlsca.org1.example.com-cert.pem
    │   └── users
    │       ├── Admin@org1.example.com
    │       │   ├── msp
    │       │   │   ├── admincerts
    │       │   │   │   └── Admin@org1.example.com-cert.pem
    │       │   │   ├── cacerts
    │       │   │   │   └── ca.org1.example.com-cert.pem
    │       │   │   ├── keystore
    │       │   │   │   └── 76cdcc8837da206a504fa9fe3314e2a7707bb9f4abbd646ba80d2553a0bdf708_sk
    │       │   │   ├── signcerts
    │       │   │   │   └── Admin@org1.example.com-cert.pem
    │       │   │   └── tlscacerts
    │       │   │       └── tlsca.org1.example.com-cert.pem
    │       │   └── tls
    │       │       ├── ca.crt
    │       │       ├── client.crt
    │       │       └── client.key
    │       └── User1@org1.example.com
    │           ├── msp
    │           │   ├── admincerts
    │           │   │   └── User1@org1.example.com-cert.pem
    │           │   ├── cacerts
    │           │   │   └── ca.org1.example.com-cert.pem
    │           │   ├── keystore
    │           │   │   └── 05dcdc6835c4cc3ea0ad9f9fdd1178fced77e2df0d6e4fe583897f233906e7a2_sk
    │           │   ├── signcerts
    │           │   │   └── User1@org1.example.com-cert.pem
    │           │   └── tlscacerts
    │           │       └── tlsca.org1.example.com-cert.pem
    │           └── tls
    │               ├── ca.crt
    │               ├── client.crt
    │               └── client.key
    └── org2.example.com
        ├── ca
        │   ├── c97317956c6b635ed4edc3b5c92fb2b67a996366038bd80424034aea8b207c20_sk
        │   └── ca.org2.example.com-cert.pem
        ├── msp
        │   ├── admincerts
        │   │   └── Admin@org2.example.com-cert.pem
        │   ├── cacerts
        │   │   └── ca.org2.example.com-cert.pem
        │   ├── config.yaml
        │   └── tlscacerts
        │       └── tlsca.org2.example.com-cert.pem
        ├── peers
        │   ├── peer0.org2.example.com
        │   │   ├── msp
        │   │   │   ├── admincerts
        │   │   │   │   └── Admin@org2.example.com-cert.pem
        │   │   │   ├── cacerts
        │   │   │   │   └── ca.org2.example.com-cert.pem
        │   │   │   ├── config.yaml
        │   │   │   ├── keystore
        │   │   │   │   └── 61d896c526a26dd6691eee10ffaa089e159eaa1e44ae6e30d8d74c255d92686b_sk
        │   │   │   ├── signcerts
        │   │   │   │   └── peer0.org2.example.com-cert.pem
        │   │   │   └── tlscacerts
        │   │   │       └── tlsca.org2.example.com-cert.pem
        │   │   └── tls
        │   │       ├── ca.crt
        │   │       ├── server.crt
        │   │       └── server.key
        │   └── peer1.org2.example.com
        │       ├── msp
        │       │   ├── admincerts
        │       │   │   └── Admin@org2.example.com-cert.pem
        │       │   ├── cacerts
        │       │   │   └── ca.org2.example.com-cert.pem
        │       │   ├── config.yaml
        │       │   ├── keystore
        │       │   │   └── 25fd5b6864d0aaec9623a9a97273d3494794dbbbccd43a14c019c8a3d10aa753_sk
        │       │   ├── signcerts
        │       │   │   └── peer1.org2.example.com-cert.pem
        │       │   └── tlscacerts
        │       │       └── tlsca.org2.example.com-cert.pem
        │       └── tls
        │           ├── ca.crt
        │           ├── server.crt
        │           └── server.key
        ├── tlsca
        │   ├── a0a3837f81d48e12f98701c088531febba3f1b9fc86eaee7ba3c653403bb0e47_sk
        │   └── tlsca.org2.example.com-cert.pem
        └── users
            ├── Admin@org2.example.com
            │   ├── msp
            │   │   ├── admincerts
            │   │   │   └── Admin@org2.example.com-cert.pem
            │   │   ├── cacerts
            │   │   │   └── ca.org2.example.com-cert.pem
            │   │   ├── keystore
            │   │   │   └── e7edce76162fd67f318676f09caa72d5dce07d97ebe78d5a5c6e64e8515ce34d_sk
            │   │   ├── signcerts
            │   │   │   └── Admin@org2.example.com-cert.pem
            │   │   └── tlscacerts
            │   │       └── tlsca.org2.example.com-cert.pem
            │   └── tls
            │       ├── ca.crt
            │       ├── client.crt
            │       └── client.key
            └── User1@org2.example.com
                ├── msp
                │   ├── admincerts
                │   │   └── User1@org2.example.com-cert.pem
                │   ├── cacerts
                │   │   └── ca.org2.example.com-cert.pem
                │   ├── keystore
                │   │   └── 6c254b083b080a4ea06b1d3033c60135b4c1893014c09cce0a88eec40e34db4c_sk
                │   ├── signcerts
                │   │   └── User1@org2.example.com-cert.pem
                │   └── tlscacerts
                │       └── tlsca.org2.example.com-cert.pem
                └── tls
                    ├── ca.crt
                    ├── client.crt
                    └── client.key

```

## genesis block
```
{
  "TwoOrgsOrdererGenesis": {
    "Capabilities": {
      "V1_1": true
    },
    "Orderer": {
      "OrdererType": "solo",
      "Addresses": [
        "orderer.example.com:7050"    (the orderer address)
      ],
      "BatchTimeout": "2s",
      "BatchSize": {
        "MaxMessageCount": 10,
        "AbsoluteMaxBytes": "99 MB",
        "PreferredMaxBytes": "512 KB"
      },
      "Kafka": {
        "Brokers": [
          "127.0.0.1:9092"
        ]
      },
      "Organizations": [
        {
          "Name": "OrdererOrg",
          "ID": "OrdererMSP",
          "MSPDir": "crypto-config/ordererOrganizations/example.com/msp"    (the msp(ca,tls,admin) used to verify participator)
        }
      ],
    },
    "Consortiums": {
      "SampleConsortium": {
        "Organizations": [
          {
            "Name": "Org1MSP",
            "ID": "Org1MSP",
            "MSPDir": "crypto-config/peerOrganizations/org1.example.com/msp",    (the msp(ca,tls,admin) used to verify org1 participator)
            "AnchorPeers": [
              {
                "Host": "peer0.org1.example.com",
                "Port": 7051
              }
            ]
          },
          {
            "Name": "Org2MSP",
            "ID": "Org2MSP",
            "MSPDir": "crypto-config/peerOrganizations/org2.example.com/msp",    (the msp(ca,tls,admin) used to verify org2 participator)
            "AnchorPeers": [
              {
                "Host": "peer0.org2.example.com",
                "Port": 7051
              }
            ]
          }
        ]
      }
    }
  }
```

## channel config transaction
```
"TwoOrgsChannel": {
  "Consortium": "SampleConsortium",
  "Application": {
    "Organizations": [
      {
        "Name": "Org1MSP",
        "ID": "Org1MSP",
        "MSPDir": "crypto-config/peerOrganizations/org1.example.com/msp",
        "AnchorPeers": [
          {
            "Host": "peer0.org1.example.com",
            "Port": 7051
          }
        ]
      },
      {
        "Name": "Org2MSP",
        "ID": "Org2MSP",
        "MSPDir": "crypto-config/peerOrganizations/org2.example.com/msp",
        "AnchorPeers": [
          {
            "Host": "peer0.org2.example.com",
            "Port": 7051
          }
        ]
      }
    ],
    "Capabilities": {
      "V1_1": true
    }
  }
}
```

## create channel
* env setup
```
#管理员local msp，拥有create channel的权限
CORE_PEER_MSPCONFIGPATH=/opt/gopath/src/github.com/hyperledger/fabric/peer/crypto/peerOrganizations/org1.example.com/users/Admin@org1.example.com/msp
CORE_PEER_ADDRESS=peer0.org1.example.com:7051
CORE_PEER_LOCALMSPID="Org1MSP"
CORE_PEER_TLS_ROOTCERT_FILE=/opt/gopath/src/github.com/hyperledger/fabric/peer/crypto/peerOrganizations/org1.example.com/peers/peer0.org1.example.com/tls/ca.crt
```

* create channel
```
export CHANNEL_NAME=mychannel
peer channel create -o orderer.example.com:7050 -c $CHANNEL_NAME -f ./channel-artifacts/channel.tx --tls --cafile /opt/gopath/src/github.com/hyperledger/fabric/peer/crypto/ordererOrganizations/example.com/orderers/orderer.example.com/msp/tlscacerts/tlsca.example.com-cert.pem
```

* peer0.org1 join channel
```
peer channel join -b mychannel.block
```

* peer0.org2 join channel
```
CORE_PEER_MSPCONFIGPATH=/opt/gopath/src/github.com/hyperledger/fabric/peer/crypto/peerOrganizations/org2.example.com/users/Admin@org2.example.com/msp CORE_PEER_ADDRESS=peer0.org2.example.com:7051
CORE_PEER_LOCALMSPID="Org2MSP" CORE_PEER_TLS_ROOTCERT_FILE=/opt/gopath/src/github.com/hyperledger/fabric/peer/crypto/peerOrganizations/org2.example.com/peers/peer0.org2.example.com/tls/ca.crt
peer channel join -b mychannel.block
```

## update channel(Update the anchor peers)
* anchor peer for Org1 -> peer0.org1.example.com  
```
peer channel update -o orderer.example.com:7050 -c $CHANNEL_NAME -f ./channel-artifacts/Org1MSPanchors.tx --tls --cafile /opt/gopath/src/github.com/hyperledger/fabric/peer/crypto/ordererOrganizations/example.com/orderers/orderer.example.com/msp/tlscacerts/tlsca.example.com-cert.pem
```

* anchor peer for Org2 -> peer0.org2.example.com
```
CORE_PEER_MSPCONFIGPATH=/opt/gopath/src/github.com/hyperledger/fabric/peer/crypto/peerOrganizations/org2.example.com/users/Admin@org2.example.com/msp CORE_PEER_ADDRESS=peer0.org2.example.com:7051 CORE_PEER_LOCALMSPID="Org2MSP" CORE_PEER_TLS_ROOTCERT_FILE=/opt/gopath/src/github.com/hyperledger/fabric/peer/crypto/peerOrganizations/org2.example.com/peers/peer0.org2.example.com/tls/ca.crt
peer channel update -o orderer.example.com:7050 -c $CHANNEL_NAME -f ./channel-artifacts/Org2MSPanchors.tx --tls --cafile /opt/gopath/src/github.com/hyperledger/fabric/peer/crypto/ordererOrganizations/example.com/orderers/orderer.example.com/msp/tlscacerts/tlsca.example.com-cert.pem
```

## Install & Instantiate Chaincode
```
peer chaincode install -n mycc -v 1.0 -p github.com/chaincode/chaincode_example02/go/

peer chaincode instantiate -o orderer.example.com:7050 --tls --cafile /opt/gopath/src/github.com/hyperledger/fabric/peer/crypto/ordererOrganizations/example.com/orderers/orderer.example.com/msp/tlscacerts/tlsca.example.com-cert.pem -C $CHANNEL_NAME -n mycc -v 1.0 -c '{"Args":["init","a", "100", "b","200"]}' -P "OR ('Org1MSP.peer','Org2MSP.peer')"
```
