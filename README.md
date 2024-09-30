# Blockchain-MRIO
pragma solidity ^0.6.0;

contract Registration{
    address payable public GRA;  // 0x20B38Da6a701c206820420dCfcB03FcB8720f206beddC4

    mapping(address=> bool) public Focal_Company; //0x4B20993Bc481177ec7E8f571ceCaE8A9e22C02db
    mapping(address=>bool) public MRIO_Data_Aggregator; //0xAb8483F64d9C6d1EcF9b849Ae677dD3315835cb2
    mapping(address => bool) public Country_1_ONS; // 0x461EDc88d0A4607e30a7a0EF6ef10F8370Dc2e6F
    mapping(address => bool) public Country_2_ONS; //0x1520a9c6Dc3a55Dc7cD06e6E6e31Fa9072047cB3
    mapping(address => bool) public Country_3_ONS; //0x78731D3Ca6b7E34aC0F824c42a7cC18A495cabaB
    mapping(address => bool) public Country_4_ONS; //0x617F2E2fD72FD9D5503197092aC168c91465E7f2
    mapping(address => bool) public RoW_ONS; //0x17F6AD8Ef982297579C203069C1DbfFE4348c372
    mapping(address=> bool) public Supplier_Om_Chm; //0x5c6B0f7Bf3E7ce046039Bd8FABdfD3f9F5021678
    mapping(address=> bool) public Supplier_Om_Poly; //0x03C6FcED478cBbC9a4FAB34eF9f40767739D1Ff7
    mapping(address=> bool) public Supplier_Ku_Poly; //0x1aE0EA34a72D944a8C7603FfB3eC30a6669E454C
    mapping(address=> bool) public Supplier_Ku_Meta; //0x0A098Eda01Ce92ff4A4CCb7A4fFFb5A43EBC70DC
    mapping(address=> bool) public Supplier_Qa_Poly; //0xCA35b7d915458EF540aDe6068dFe2F44E8fa733c
    mapping(address=> bool) public Supplier_Qa_Meta_1; //0x14723A09ACff6D2A60DcdF7aA4AFf308FDDC160C
    mapping(address=> bool) public Supplier_Qa_Meta_2; //0x4B0897b0513fdC7C541B6d9D7E929C4e5364D2dB
    mapping(address=> bool) public Supplier_Ae_Chm_1; //0x583031D1113aD414F02576BD6afaBfb302140225
    mapping(address=> bool) public Supplier_Ae_Chm_2; //0xdD870fA1b7C4700F2BD7f44238821C26f7392148

    mapping(address=> bool) public Supplier_Ae_Chm_3; //0x55a1Dd406d51c6B6827c3940A63c03cb113F8Ad7
    mapping(address=> bool) public Supplier_Ae_Ele; //0x71213191Aa7Fca82f493Cb0f9cc6de6a7ef2Eb9E
    mapping(address=> bool) public Supplier_RoW_Meta; //0x6eCd876c6BCC749Eae80803eEFFdA155fEd2eabd
    



    modifier onlyGRA{
        require(msg.sender == GRA, "Sender not authorized.");
        _;
    }   
    
    constructor() public{
        GRA = msg.sender;
    }
    
    
    function registerCountry_1_ONS(address C1) external onlyGRA {
        require(!Country_1_ONS[C1], "Country_1_ONS exists already");
        Country_1_ONS[C1] = true;
    }
    
    function registerCountry_2_ONS(address C2) external onlyGRA {
        require(!Country_2_ONS[C2], "Country_2_ONS exists already");
        Country_2_ONS[C2] = true;
    }
    
    function registerCountry_3_ONS(address C3) external onlyGRA {
        require(!Country_3_ONS[C3], "Country_3_ONS exists already");
        Country_3_ONS[C3] = true;
    }
    
    function registerCountry_4_ONS(address C4) external onlyGRA {
        require(!Country_4_ONS[C4], "Country_4_ONS exists already");
        Country_4_ONS[C4] = true;
    }
    
    function registerRoW_ONS(address C5) external onlyGRA {
        require(!RoW_ONS[C5], "RoW exists already");
        RoW_ONS[C5] = true;
    }

    function registerSupplier_Om_Chm(address S1) external onlyGRA{
        require(!Supplier_Om_Chm[S1], "Supplier_Om_Chm exists already");
        Supplier_Om_Chm[S1] =true;
    }

    function registerSupplier_Om_Poly(address P1) external onlyGRA{
        require(!Supplier_Om_Poly[P1], "Supplier_Om_Poly exists already");
        Supplier_Om_Poly[P1] =true;
    }

    function registerSupplier_Ku_Poly(address P2) external onlyGRA{
        require(!Supplier_Ku_Poly[P2], "Supplier_Ku_Poly exists already");
        Supplier_Ku_Poly[P2] =true;
    }

    function registerSupplier_Ku_Meta(address M1) external onlyGRA{
        require(!Supplier_Ku_Meta[M1], "Supplier_Ku_Meta exists already");
        Supplier_Ku_Meta[M1] =true;
    }

    function registerSupplier_Qa_Poly(address P3) external onlyGRA{
        require(!Supplier_Qa_Poly[P3], "Supplier_Qa_Poly exists already");
        Supplier_Qa_Poly[P3] =true;
    }

    function registerSupplier_Qa_Meta_1(address M1) external onlyGRA{
        require(!Supplier_Qa_Meta_1[M1], "Supplier_Qa_Meta_1 exists already");
        Supplier_Qa_Meta_1[M1] =true;
    }

    function registerSupplier_Qa_Meta_2(address M2) external onlyGRA{
        require(!Supplier_Qa_Meta_2[M2], "Supplier_Qa_Meta_2 exists already");
        Supplier_Qa_Meta_2[M2] =true;
    }

    function registerSupplier_Ae_Chm_1(address C1) external onlyGRA{
        require(!Supplier_Ae_Chm_1[C1], "Supplier_Ae_Chm_1 exists already");
        Supplier_Ae_Chm_1[C1] =true;
    }

    function registerSupplier_Ae_Chm_2(address C2) external onlyGRA{
        require(!Supplier_Ae_Chm_2[C2], "Supplier_Ae_Chm_2 exists already");
        Supplier_Ae_Chm_2[C2] =true;
    }

    function registerSupplier_Ae_Chm_3(address C3) external onlyGRA{
        require(!Supplier_Ae_Chm_3[C3], "Supplier_Ae_Chm_3 exists already");
        Supplier_Ae_Chm_3[C3] =true;
    }

    function registerSupplier_Ae_Ele(address E1) external onlyGRA{
        require(!Supplier_Ae_Ele[E1], "Supplier_Ae_Ele exists already");
        Supplier_Ae_Ele[E1] =true;
    }

    function registerSupplier_RoW_Meta(address M3) external onlyGRA{
        require(!Supplier_RoW_Meta[M3], "Supplier_RoW_Meta exists already");
        Supplier_RoW_Meta[M3] =true;
    }

    function registerFocal_Company(address F) external onlyGRA{
        require(!Focal_Company[F], "Focal_Company exists already");
        Focal_Company[F] =true;
    }

    function registerMRIO_Data_Aggregator(address A) external onlyGRA{
        require(!MRIO_Data_Aggregator[A], "MRIO_Data_Aggregator exists already");
        MRIO_Data_Aggregator[A] =true;
    }


    
    
    function isGRA(address g) public view returns(bool) {
        return (GRA == g);
    }
    
    function Country_1_ONSExists(address C1) public view returns(bool) {
        return Country_1_ONS[C1];
    }

    function Country_2_ONSExists(address C2) public view returns(bool) {
        return Country_2_ONS[C2];
    }

    function Country_3_ONSExists(address C3) public view returns(bool) {
        return Country_3_ONS[C3];
    }

    function Country_4_ONSExists(address C4) public view returns(bool) {
        return Country_4_ONS[C4];
    }
    
    function RoW_ONSExists(address C5) public view returns(bool) {
        return RoW_ONS[C5];
    }
    
        
    function Supplier_Om_ChmExists(address S1) public view returns(bool) {
        return Supplier_Om_Chm[S1];
    }


    function Supplier_Om_PolyExists(address P1) public view returns(bool) {
        return Supplier_Om_Poly[P1];
    }

    function Supplier_Ku_PolyExists(address P2) public view returns(bool) {
        return Supplier_Ku_Poly[P2];
    }

    function Supplier_Ku_MetaExists(address M1) public view returns(bool) {
        return Supplier_Ku_Meta[M1];
    }

    function Supplier_Qa_PolyExists(address P3) public view returns(bool) {
        return Supplier_Qa_Poly[P3];
    }

    function Supplier_Qa_Meta_1Exists(address M1) public view returns(bool) {
        return Supplier_Qa_Meta_1[M1];
    }

    function Supplier_Qa_Meta_2Exists(address M2) public view returns(bool) {
        return Supplier_Qa_Meta_2[M2];
    }

    function Supplier_Ae_Chm_1Exists(address C1) public view returns(bool) {
        return Supplier_Ae_Chm_1[C1];
    }

    function Supplier_Ae_Chm_2Exists(address C2) public view returns(bool) {
        return Supplier_Ae_Chm_2[C2];
    }

    function Supplier_Ae_Chm_3Exists(address C3) public view returns(bool) {
        return Supplier_Ae_Chm_3[C3];
    }

    function Supplier_Ae_EleExists(address E1) public view returns(bool) {
        return Supplier_Ae_Ele[E1];
    }

    function Supplier_RoW_MetaExists(address M3) public view returns(bool) {
        return Supplier_RoW_Meta[M3];
    }

    function Focal_CompanyExists(address F) public view returns(bool) {
        return Focal_Company[F];
    }

    function MRIO_Data_AggregatorExists(address A) public view returns(bool) {
        return MRIO_Data_Aggregator[A];
    }

}

contract InputOutputIntermediateConsumption{

     
     Registration public registrationContract;
     address payable public MRIO_Data_Aggregator;
     constructor(address registration) public {
        registrationContract = Registration(registration);
        
        require(registrationContract.MRIO_Data_AggregatorExists(msg.sender), "Sender not authorized");
        MRIO_Data_Aggregator = payable(msg.sender);
    }
    modifier onlyMRIO_Data_Aggregator {
        require(registrationContract.MRIO_Data_AggregatorExists(msg.sender), "Sender not authorized");
        _;
    }
    modifier onlyCountry_1_ONS {
        require(
            registrationContract.Country_1_ONSExists(msg.sender),
            "Sender not authorized"
        );
        _;
    }

    modifier onlyCountry_2_ONS {
        require(
            registrationContract.Country_2_ONSExists(msg.sender),
            "Sender not authorized"
        );
        _;
    }

    modifier onlyCountry_3_ONS {
        require(
            registrationContract.Country_3_ONSExists(msg.sender),
            "Sender not authorized"
        );
        _;
    }

    modifier onlyCountry_4_ONS {
        require(
            registrationContract.Country_4_ONSExists(msg.sender),
            "Sender not authorized"
        );
        _;
    }

    modifier onlyRoW_ONS {
        require(
            registrationContract.RoW_ONSExists(msg.sender),
            "Sender not authorized"
        );
        _;
    }

    modifier onlySupplier_Om_Chm {
        require(
            registrationContract.Supplier_Om_ChmExists(msg.sender),
            "Sender not authorized"
        );
        _;
    }

    modifier onlySupplier_Om_Poly {
        require(
            registrationContract.Supplier_Om_PolyExists(msg.sender),
            "Sender not authorized"
        );
        _;
    }

    modifier onlySupplier_Ku_Poly {
        require(
            registrationContract.Supplier_Ku_PolyExists(msg.sender),
            "Sender not authorized"
        );
        _;
    }

    modifier onlySupplier_Ku_Meta {
        require(
            registrationContract.Supplier_Ku_MetaExists(msg.sender),
            "Sender not authorized"
        );
        _;
    }

    modifier onlySupplier_Qa_Poly {
        require(
            registrationContract.Supplier_Qa_PolyExists(msg.sender),
            "Sender not authorized"
        );
        _;
    }

    modifier onlySupplier_Qa_Meta_1 {
        require(
            registrationContract.Supplier_Qa_Meta_1Exists(msg.sender),
            "Sender not authorized"
        );
        _;
    }

    modifier onlySupplier_Qa_Meta_2 {
        require(
            registrationContract.Supplier_Qa_Meta_2Exists(msg.sender),
            "Sender not authorized"
        );
        _;
    }

    modifier onlySupplier_Ae_Chm_1 {
        require(
            registrationContract.Supplier_Ae_Chm_1Exists(msg.sender),
            "Sender not authorized"
        );
        _;
    }

     modifier onlySupplier_Ae_Chm_2 {
        require(
            registrationContract.Supplier_Ae_Chm_2Exists(msg.sender),
            "Sender not authorized"
        );
        _;
    }

     modifier onlySupplier_Ae_Chm_3 {
        require(
            registrationContract.Supplier_Ae_Chm_3Exists(msg.sender),
            "Sender not authorized"
        );
        _;
    }
     modifier onlySupplier_Ae_Ele{
        require(
            registrationContract.Supplier_Ae_EleExists(msg.sender),
            "Sender not authorized"
        );
        _;
    }
     modifier onlySupplier_RoW_Meta {
        require(
            registrationContract.Supplier_RoW_MetaExists(msg.sender),
            "Sender not authorized"
        );
        _;
    }

    modifier onlyFocalCompany {
        require(
            registrationContract.Focal_CompanyExists(msg.sender),
            "Sender not authorized"
        );
        _;
    }

    event Country_1_ICM_Updated(uint[20][4] matrixZ1);
    function UpdateCountry_1_ICM(uint[20][4] memory matrixZ1) public onlyCountry_1_ONS {
    emit Country_1_ICM_Updated(matrixZ1);

}

    event Country_2_ICM_Updated(uint[20][4] matrixZ2);
    function UpdateCountry_2_ICM(uint[20][4] memory matrixZ2) public onlyCountry_2_ONS {
        emit Country_2_ICM_Updated(matrixZ2);
    }

    event Country_3_ICM_Updated(uint[20][4] matrixZ3);
    function UpdateCountry_3_ICM(uint[20][4] memory matrixZ3) public onlyCountry_3_ONS {
        emit Country_3_ICM_Updated(matrixZ3);
    }

    event Country_4_ICM_Updated(uint[20][4] matrixZ4);
    function UpdateCountry_4_ICM(uint[20][4] memory matrixZ4) public onlyCountry_4_ONS {
        emit Country_4_ICM_Updated(matrixZ4);
    }

    event RoW_ICM_Updated(uint[20][4] matrixZ5);
    function UpdateRoW_ICM(uint[20][4] memory matrixZ5) public onlyRoW_ONS {
        emit RoW_ICM_Updated(matrixZ5);

    }


  event FinalICMUpdated(uint[20][20] MatrixZ);

function createFinalICM(uint[20][20] memory MatrixZ) public onlyMRIO_Data_Aggregator returns (uint[20][20] memory){  
    
    emit FinalICMUpdated(MatrixZ);

    
    return MatrixZ;
}



    event  Om_ChmDemandUpdated(uint Y1);
    function Input_Om_ChmDemand(uint Y1) public onlySupplier_Om_Chm {
    emit Om_ChmDemandUpdated(Y1);
    }

    event  Om_PolyDemandUpdated(uint Y2);
    function Input_Om_PolyDemand(uint Y2) public onlySupplier_Om_Poly {
    emit Om_PolyDemandUpdated(Y2);
    }
    event  Ku_PolyDemandUpdated(uint Y3);
    function Input_Ku_PolyDemand(uint Y3) public onlySupplier_Ku_Poly {
    emit Ku_PolyDemandUpdated(Y3);
    }
    event  Ku_MetaDemandUpdated(uint Y4);
    function Input_Ku_MetaDemand(uint Y4) public onlySupplier_Ku_Meta {
    emit Ku_MetaDemandUpdated(Y4);
    }
    event  Qa_PolyDemandUpdated(uint Y5);
    function Input_Qa_PolyDemand(uint Y5) public onlySupplier_Qa_Poly {
    emit Qa_PolyDemandUpdated(Y5);
    }
    event  Qa_Meta_1DemandUpdated(uint Y6);
    function Input_Qa_Meta_1Demand(uint Y6) public onlySupplier_Qa_Meta_1 {
    emit Qa_Meta_1DemandUpdated(Y6);
    }
    event  Qa_Meta_2DemandUpdated(uint Y7);
    function Input_Qa_Meta_2Demand(uint Y7) public onlySupplier_Qa_Meta_2 {
    emit Qa_Meta_2DemandUpdated(Y7);
    }

    event  Ae_Chm_1DemandUpdated(uint Y8);
    function Input_Chm_1Demand(uint Y8) public onlySupplier_Ae_Chm_1 {
    emit Ae_Chm_1DemandUpdated(Y8);
    }

    event  Ae_Chm_2DemandUpdated(uint Y9);
    function Input_Chm_2Demand(uint Y9) public onlySupplier_Ae_Chm_2 {
    emit Ae_Chm_2DemandUpdated(Y9);
    }

    event  Ae_Chm_3DemandUpdated(uint Y10);
    function Input_Chm_3Demand(uint Y10) public onlySupplier_Ae_Chm_3 {
    emit Ae_Chm_3DemandUpdated(Y10);
    }

    event  Ae_EleDemandUpdated(uint Y11);
    function Input_Ae_EleDemand(uint Y11) public onlySupplier_Ae_Ele {
    emit Ae_EleDemandUpdated(Y11);
    }

    event  RoW_MetaDemandUpdated(uint Y12);
    function Input_RoW_MetaDemand(uint Y12) public onlySupplier_RoW_Meta {
    emit RoW_MetaDemandUpdated(Y12);
    }


}
contract ProductionandConsumptionImpactAssessment{

    InputOutputIntermediateConsumption public InputOutputIntermediateconsumptionContract;
    Registration public registrationContract;

     address payable public Focal_Company;
     constructor(address registration) public {
        registrationContract = Registration(registration);
        
        require(registrationContract.Focal_Company(msg.sender), "Sender not authorized");
        Focal_Company = payable(msg.sender);
    }

    modifier onlyFocal_Company {
        require(registrationContract.Focal_Company(msg.sender), "Sender not authorized");
        _;
    }

  event TCMCalculated(uint[20][20] matrixA);

function calculateTCM(
    uint[20][20] memory matrixZ, 
    uint[20][20] memory matrixX
) 
    public 
    onlyFocal_Company 
    returns (uint[20][20] memory) 
{
    uint[20][20] memory matrixA;
    uint scalingFactor = 10000; 

    for (uint i = 0; i < 20; i++) {
        for (uint j = 0; j < 20; j++) {
            require(matrixX[i][j] != 0, "Divisor cannot be zero");
            
            
            matrixA[i][j] = (matrixZ[i][j] * scalingFactor) / matrixX[i][j];

        }
    }

    
    emit TCMCalculated(matrixA);

    return matrixA;
}

    event LIMUpdated(uint[20][20] matrixL);

function inputLIM(uint[20][20] memory matrixL) 
    public 
    onlyFocal_Company 
    returns (uint[20][20] memory) 
{
    
    emit LIMUpdated(matrixL);
    
   
    return matrixL;
}



event DIMCalculated(uint[20] matrixE_int);

function calculateDIM(
    uint[20] memory matrixE, 
    uint[20] memory divisors
) 
    public 
    onlyFocal_Company 
    returns (uint[20] memory) 
{
    
    uint[20] memory MatrixE_int;
    uint scalingFactor = 10**6;  

    
    for (uint i = 0; i < 20; i++) {
        require(divisors[i] != 0, "Division by zero");  
        
        
        MatrixE_int[i] = (matrixE[i] * scalingFactor) / divisors[i];
    }

    
    emit DIMCalculated(MatrixE_int);

    
    return MatrixE_int;
}
   event TIMCalculated(uint[20][20] matrixT);

function CalculateTIM(
    uint[20][20] memory matrixE, 
    uint[20][20] memory matrixL
) 
    public 
    onlyFocal_Company 
    returns (uint[20][20] memory) 
{
    uint[20][20] memory matrixT;
    uint scalingFactor = 10**7;  

    
    for (uint i = 0; i < 20; i++) {
        for (uint j = 0; j < 20; j++) {
            matrixT[i][j] = 0;  

            
            for (uint k = 0; k < 20; k++) {
                matrixT[i][j] += (matrixE[i][k] * matrixL[k][j]);
            }

            
            matrixT[i][j] = matrixT[i][j] / scalingFactor;
        }
    }

    
    emit TIMCalculated(matrixT);

    
    return matrixT;
}

    event Production_basedImpactCalculated(uint[20][20] matrixX1);

function calculateProduction_basedImpact(
    uint[20][20] memory matrixE, 
    uint[20][20] memory matrixY
) 
    public 
    returns (uint[20][20] memory) 
{
    uint[20][20] memory matrixX1;  

    
    for (uint i = 0; i < 20; i++) {
        for (uint j = 0; j < 20; j++) {
            matrixX1[i][j] = 0;  

            
            for (uint k = 0; k < 20; k++) {
                matrixX1[i][j] += matrixE[i][k] * matrixY[k][j];  // Multiply and sum elements
            }
        }
    }

    
    emit Production_basedImpactCalculated(matrixX1);

    
    return matrixX1;
}

  event Consumption_basedImpactCalculated(uint[20][20] matrixX3);

function calculateConsumption_basedImpact(
    uint[20][20] memory matrixE, 
    uint[20][20] memory matrixL, 
    uint[20][20] memory matrixY
) 
    public 
    returns (uint[20][20] memory) 
{
    uint[20][20] memory matrixIntermediate; 
    uint[20][20] memory matrixX3;            
    uint scalingFactor = 10000000;           


    for (uint i = 0; i < 20; i++) {
        for (uint j = 0; j < 20; j++) {
            matrixIntermediate[i][j] = 0;  
            for (uint k = 0; k < 20; k++) {
                matrixIntermediate[i][j] += matrixE[i][k] * matrixL[k][j];
            }
        }
    }

   
    for (uint i = 0; i < 20; i++) {
        for (uint j = 0; j < 20; j++) {
            matrixX3[i][j] = 0;  
            for (uint k = 0; k < 20; k++) {
                matrixX3[i][j] += matrixIntermediate[i][k] * matrixY[k][j];
            }

            
            matrixX3[i][j] = matrixX3[i][j] / scalingFactor;
        }
    }

   
    emit Consumption_basedImpactCalculated(matrixX3);

    
    return matrixX3;
    }
}
