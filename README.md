// SPDX-License-Identifier: MIT

pragma solidity ^0.8.20;

contract Registration {
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

    mapping(address=> bool) public Supplier_Ae_Chm_3; //0x117D0500e5B5131a17013834662A23190c2307FE
    mapping(address=> bool) public Supplier_Ae_Ele; //0xC973C05FEDfCA9f028e4f911F9f4C512e8EAE366
    mapping(address=> bool) public Supplier_RoW_Meta; //0x98a2e346bb348D00bcA78C75628e8F3946a7e224

    modifier onlyGRA{
        require(msg.sender == GRA, "Sender not authorized.");
         _;
    }  

   constructor() payable {
    GRA = payable(msg.sender);
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

    function registerSupplier_Ae_Chm_1(address Ch1) external onlyGRA{
        require(!Supplier_Ae_Chm_1[Ch1], "Supplier_Ae_Chm_1 exists already");
        Supplier_Ae_Chm_1[Ch1] =true;
    }

    function registerSupplier_Ae_Chm_2(address Ch2) external onlyGRA{
        require(!Supplier_Ae_Chm_2[Ch2], "Supplier_Ae_Chm_2 exists already");
        Supplier_Ae_Chm_2[Ch2] =true;
    }

    function registerSupplier_Ae_Chm_3(address Ch3) external onlyGRA{
        require(!Supplier_Ae_Chm_3[Ch3], "Supplier_Ae_Chm_3 exists already");
        Supplier_Ae_Chm_3[Ch3] =true;
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

    function Supplier_Ae_Chm_1Exists(address Ch1) public view returns(bool) {
        return Supplier_Ae_Chm_1[Ch1];
    }

    function Supplier_Ae_Chm_2Exists(address Ch2) public view returns(bool) {
        return Supplier_Ae_Chm_2[Ch2];
    }

    function Supplier_Ae_Chm_3Exists(address Ch3) public view returns(bool) {
        return Supplier_Ae_Chm_3[Ch3];
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

contract InputOutputIntermediateConsumption {
    Registration public registrationContract;
    constructor(address registrationAddress) {
        registrationContract = Registration(registrationAddress);
    }
    modifier onlyCountry_1_ONS() {
        require(registrationContract.Country_1_ONSExists(msg.sender),
            "Sender not authorized"
        );
        _;
    }
    modifier onlyCountry_2_ONS() {
        require(registrationContract.Country_2_ONSExists(msg.sender),
            "Sender not authorized");
        _;
    }
    modifier onlyCountry_3_ONS() {
        require(registrationContract.Country_3_ONSExists(msg.sender),
            "Sender not authorized");
        _;
    }

    modifier onlyCountry_4_ONS() {
        require(registrationContract.Country_4_ONSExists(msg.sender),
            "Sender not authorized");
        _;
    }

    modifier onlyRoW_ONS() {
        require(registrationContract.RoW_ONSExists(msg.sender),
            "Sender not authorized");
        _;
    }

    modifier onlyMRIO_Data_Aggregator() {
        require(registrationContract.MRIO_Data_AggregatorExists(msg.sender),
            "Sender not authorized");
        _;
    }

    modifier onlyFocalCompany() {
        require(registrationContract.Focal_CompanyExists(msg.sender),
            "Sender not authorized"
        );
        _;
    }

    modifier onlySupplier_Om_Chm() {
        require(registrationContract.Supplier_Om_ChmExists(msg.sender),
            "Sender not authorized"
        );
        _;
    }
    modifier onlySupplier_Om_Poly() {
        require(registrationContract.Supplier_Om_PolyExists(msg.sender),
            "Sender not authorized"
        );
        _;
    }

    modifier onlySupplier_Ku_Poly() {
        require(registrationContract.Supplier_Ku_PolyExists(msg.sender),
            "Sender not authorized"
        );
        _;
    }

    modifier onlySupplier_Ku_Meta() {
        require(registrationContract.Supplier_Ku_MetaExists(msg.sender),
            "Sender not authorized"
        );
        _;
    }
    modifier onlySupplier_Qa_Poly() {
        require(registrationContract.Supplier_Qa_PolyExists(msg.sender),
            "Sender not authorized"
        );
        _;
    }
    modifier onlySupplier_Qa_Meta_1() {
        require(registrationContract.Supplier_Qa_Meta_1Exists(msg.sender),
            "Sender not authorized"
        );
        _;
    }
    modifier onlySupplier_Qa_Meta_2() {
        require(registrationContract.Supplier_Qa_Meta_2Exists(msg.sender),
            "Sender not authorized"
        );
        _;
    }
    modifier onlySupplier_Ae_Chm_1() {
        require(registrationContract.Supplier_Ae_Chm_1Exists(msg.sender),
            "Sender not authorized"
        );
        _;
    }
    modifier onlySupplier_Ae_Chm_2() {
        require(registrationContract.Supplier_Ae_Chm_2Exists(msg.sender),
            "Sender not authorized"
        );
        _;
    }
    modifier onlySupplier_Ae_Chm_3() {
        require(registrationContract.Supplier_Ae_Chm_3Exists(msg.sender),
            "Sender not authorized"
        );
        _;
    }
    modifier onlySupplier_Ae_Ele() {
        require(registrationContract.Supplier_Ae_EleExists(msg.sender),
            "Sender not authorized"
        );
        _;
    }
    modifier onlySupplier_RoW_Meta() {
        require(registrationContract.Supplier_RoW_MetaExists(msg.sender),
            "Sender not authorized"
        );
        _;
    }

    event Country_1_ICM_Updated(uint256[20][4] matrixZ1);

    function UpdateCountry_1_ICM(uint256[20][4] memory matrixZ1) public onlyCountry_1_ONS {
        emit Country_1_ICM_Updated(matrixZ1);
    }

    event Country_2_ICM_Updated(uint256[20][4] matrixZ2);

    function UpdateCountry_2_ICM(uint256[20][4] memory matrixZ2) public onlyCountry_2_ONS {
        emit Country_2_ICM_Updated(matrixZ2);
    }

    event Country_3_ICM_Updated(uint256[20][4] matrixZ3);

    function UpdateCountry_3_ICM(uint256[20][4] memory matrixZ3) public onlyCountry_3_ONS {
        emit Country_3_ICM_Updated(matrixZ3);
    }

    event Country_4_ICM_Updated(uint256[20][4] matrixZ4);
    function UpdateCountry_4_ICM(uint256[20][4] memory matrixZ4) public onlyCountry_4_ONS {
        emit Country_4_ICM_Updated(matrixZ4);
    }

    event RoW_ICM_Updated(uint256[20][4] matrixZ5);
    function UpdateRoW_ICM(uint256[20][4] memory matrixZ5) public onlyRoW_ONS {
        emit RoW_ICM_Updated(matrixZ5);
    }

    event FinalICMUpdated(uint256[20][20] MatrixZ);
    function createFinalICM(uint256[20][20] memory MatrixZ)   public onlyMRIO_Data_Aggregator
        returns (uint256[20][20] memory)
    {
        emit FinalICMUpdated(MatrixZ);
        return MatrixZ;
    }

    event Om_ChmDemandUpdated(uint256 Y1);
    function Input_Om_ChmDemand(uint256 Y1) public onlySupplier_Om_Chm {
        emit Om_ChmDemandUpdated(Y1);
    }

    event Om_PolyDemandUpdated(uint256 Y2);
    function Input_Om_PolyDemand(uint256 Y2) public onlySupplier_Om_Poly {
        emit Om_PolyDemandUpdated(Y2);
    }

    event Ku_PolyDemandUpdated(uint256 Y3);
    function Input_Ku_PolyDemand(uint256 Y3) public onlySupplier_Ku_Poly {
        emit Ku_PolyDemandUpdated(Y3);
    }

    event Ku_MetaDemandUpdated(uint256 Y4);
    function Input_Ku_MetaDemand(uint256 Y4) public onlySupplier_Ku_Meta {
        emit Ku_MetaDemandUpdated(Y4);
    }

    event Qa_PolyDemandUpdated(uint256 Y5);
    function Input_Qa_PolyDemand(uint256 Y5) public onlySupplier_Qa_Poly {
        emit Qa_PolyDemandUpdated(Y5);
    }

    event Qa_Meta_1DemandUpdated(uint256 Y6);
    function Input_Qa_Meta_1Demand(uint256 Y6) public onlySupplier_Qa_Meta_1 {
        emit Qa_Meta_1DemandUpdated(Y6);
    }

    event Qa_Meta_2DemandUpdated(uint256 Y7);
    function Input_Qa_Meta_2Demand(uint256 Y7) public onlySupplier_Qa_Meta_2 {
        emit Qa_Meta_2DemandUpdated(Y7);
    }

    event Ae_Chm_1DemandUpdated(uint256 Y8);
    function Input_Chm_1Demand(uint256 Y8) public onlySupplier_Ae_Chm_1 {
        emit Ae_Chm_1DemandUpdated(Y8);
    }

    event Ae_Chm_2DemandUpdated(uint256 Y9);
    function Input_Chm_2Demand(uint256 Y9) public onlySupplier_Ae_Chm_2 {
        emit Ae_Chm_2DemandUpdated(Y9);
    }

    event Ae_Chm_3DemandUpdated(uint256 Y10);
    function Input_Chm_3Demand(uint256 Y10) public onlySupplier_Ae_Chm_3 {
        emit Ae_Chm_3DemandUpdated(Y10);
    }

    event Ae_EleDemandUpdated(uint256 Y11);
    function Input_Ae_EleDemand(uint256 Y11) public onlySupplier_Ae_Ele {
        emit Ae_EleDemandUpdated(Y11);
    }

    event RoW_MetaDemandUpdated(uint256 Y12);
    function Input_RoW_MetaDemand(uint256 Y12) public onlySupplier_RoW_Meta {
        emit RoW_MetaDemandUpdated(Y12);
    }
}


contract ProductionandConsumptionImpactAssessment {
    Registration public registrationContract;

    uint256 public constant N = 20;
    uint256 public constant SCALE_1 = 1e5;
    uint256 public constant SCALE_2 = 1e6;
    uint256 public constant SCALE_3 = 1e11;
    address payable public Focal_Company;

    uint256[20][20] public lastTCM;
    uint256[20][20] public lastLIM;
    uint256[20] public lastDIM;
    uint256[20][20] public lastTIM;
    uint256[20][20] public lastProductionImpact;
    uint256[20][20] public lastConsumptionImpact;

    event TCMCalculated(uint256[20][20] matrixA);
    event LIMUpdated(uint256[20][20] matrixL);
    event DIMCalculated(uint256[20] matrixE_int);
    event TIMCalculated(uint256[20][20] matrixT);
    event Production_basedImpactCalculated(uint256[20][20] matrixX1);
    event Consumption_basedImpactCalculated(uint256[20][20] matrixX3);

    constructor(address registration) {
        registrationContract = Registration(registration);
        require(
            registrationContract.Focal_Company(msg.sender) ||
                registrationContract.Focal_CompanyExists(msg.sender),
            "Sender not authorized"
        );
        Focal_Company = payable(msg.sender);
    }

    modifier onlyFocal_Company() {
        require(registrationContract.Focal_CompanyExists(msg.sender),
            "Sender not authorized"
        );
        _;
    }


    function calculateTCM(
        uint256[20][20] calldata matrixZ,
        uint256[20] calldata vectorX
    )
        public
        onlyFocal_Company
        returns (uint256[20][20] memory matrixA)
    {
        for (uint256 j = 0; j < N; j++) {
            require(vectorX[j] != 0, "Column divisor cannot be zero");
        }

        for (uint256 i = 0; i < N; i++) {
            for (uint256 j = 0; j < N; j++) {
                matrixA[i][j] = (matrixZ[i][j] * SCALE_1) / vectorX[j];
            }
        }

        lastTCM = matrixA;
        emit TCMCalculated(matrixA);
        return matrixA;
    }


    function computeLIM_NeumannSeries(
        uint256[20][20] calldata A,
        uint256 K
    )
        public
        onlyFocal_Company
        returns (uint256[20][20] memory L)
    {
        require(K > 0 && K <= 50, "K out of range");

        L = _identity();

        uint256[20][20] memory P = A;
        _addInPlace(L, P);

        for (uint256 k = 2; k <= K; k++) {
            P = _mulFixed(P, A);
            _addInPlace(L, P);
        }

        lastLIM = L;
        emit LIMUpdated(L);
        return L;
    }

    function computeStoredTCM_LIM(
        uint256 K
    )
        external
        onlyFocal_Company
        returns (uint256[20][20] memory L)
    {
        require(K > 0 && K <= 50, "K out of range");

        uint256[20][20] memory A = lastTCM;

        L = _identity();

        uint256[20][20] memory P = A;
        _addInPlace(L, P);

        for (uint256 k = 2; k <= K; k++) {
            P = _mulFixed(P, A);
            _addInPlace(L, P);
        }

        lastLIM = L;
        emit LIMUpdated(L);
        return L;
    }

 
    function calculateDIM(
        uint256[20] calldata matrixE,
        uint256[20] calldata divisors
    )
        external
        onlyFocal_Company
        returns (uint256[20] memory MatrixE_int)
    {
        for (uint256 i = 0; i < N; i++) {
            require(divisors[i] != 0, "Division by zero");
            MatrixE_int[i] = (matrixE[i] * SCALE_2) / divisors[i];
        }

        lastDIM = MatrixE_int;
        emit DIMCalculated(MatrixE_int);
        return MatrixE_int;
    }

    function calculateTIM(
        uint256[20][20] calldata matrixL,
        uint256[20] calldata matrixDIM
    )
        external
        onlyFocal_Company
        returns (uint256[20][20] memory matrixT)
    {
        for (uint256 i = 0; i < N; i++) {
            for (uint256 j = 0; j < N; j++) {
                matrixT[i][j] = (matrixL[i][j] * matrixDIM[i]);
            }
        }

        lastTIM = matrixT;
        emit TIMCalculated(matrixT);
        return matrixT;
    }

    function calculateStoredTIM()
        external
        onlyFocal_Company
        returns (uint256[20][20] memory matrixT)
    {
        uint256[20] memory matrixDIM = lastDIM;
        uint256[20][20] memory matrixL = lastLIM;

        for (uint256 i = 0; i < N; i++) {
            for (uint256 j = 0; j < N; j++) {
                matrixT[i][j] = (matrixDIM[i] * matrixL[i][j]);
            }
        }

        lastTIM = matrixT;
        emit TIMCalculated(matrixT);
        return matrixT;
    }

  
    function calculateProduction_basedImpact(
        uint256[20] calldata matrixDIM,
        uint256[20][20] calldata matrixY
    )
        external
        onlyFocal_Company
        returns (uint256[20][20] memory matrixX1)
    {
        for (uint256 i = 0; i < N; i++) {
            for (uint256 j = 0; j < N; j++) {
                matrixX1[i][j] = ((matrixDIM[i] * matrixY[i][j])*100) / SCALE_1;
            }
        }

        lastProductionImpact = matrixX1;
        emit Production_basedImpactCalculated(matrixX1);
        return matrixX1;
    }


    function calculateStoredProduction_basedImpact(
        uint256[20][20] calldata matrixY
    )
        external
        onlyFocal_Company
        returns (uint256[20][20] memory matrixX1)
    {
        uint256[20] memory matrixDIM = lastDIM;

        for (uint256 i = 0; i < N; i++) {
            for (uint256 j = 0; j < N; j++) {
                matrixX1[i][j] = (matrixDIM[i] * matrixY[i][j]*100) / SCALE_1;
            }
        }

        lastProductionImpact = matrixX1;
        emit Production_basedImpactCalculated(matrixX1);
        return matrixX1;
    }


    function calculateConsumption_basedImpact(
        uint256[20][20] calldata matrixT,
        uint256[20][20] calldata matrixY
    )
        external
        onlyFocal_Company
        returns (uint256[20][20] memory matrixX3)
    {
        for (uint256 i = 0; i < N; i++) {
            for (uint256 j = 0; j < N; j++) {
                uint256 sum = 0;
                for (uint256 k = 0; k < N; k++) {
                    sum += (matrixT[i][k] * matrixY[k][j]) *1000 / SCALE_3;
                }
                matrixX3[i][j] = sum;
            }
        }

        lastConsumptionImpact = matrixX3;
        emit Consumption_basedImpactCalculated(matrixX3);
        return matrixX3;
    }


    function calculateStoredConsumption_basedImpact(
        uint256[20][20] calldata matrixY
    )
        external
        onlyFocal_Company
        returns (uint256[20][20] memory matrixX3)
    {
        uint256[20][20] memory matrixT = lastTIM;

        for (uint256 i = 0; i < N; i++) {
            for (uint256 j = 0; j < N; j++) {
                uint256 sum = 0;
                for (uint256 k = 0; k < N; k++) {
                    sum += (matrixT[i][k] * matrixY[k][j])*1000 / SCALE_3;
                }
                matrixX3[i][j] = sum;
            }
        }

        lastConsumptionImpact = matrixX3;
        emit Consumption_basedImpactCalculated(matrixX3);
        return matrixX3;
    }


    function runFullAssessment(
        uint256[20][20] calldata matrixZ,
        uint256[20] calldata vectorX,
        uint256 K,
        uint256[20] calldata matrixE,
        uint256[20][20] calldata matrixY
    )
        external
        onlyFocal_Company
        returns (
            uint256[20][20] memory matrixA,
            uint256[20][20] memory matrixL,
            uint256[20] memory matrixDIM,
            uint256[20][20] memory matrixT,
            uint256[20][20] memory matrixPB,
            uint256[20][20] memory matrixCB
        )
    {
        require(K > 0 && K <= 50, "K out of range");

        // TCM
        for (uint256 j = 0; j < N; j++) {
            require(vectorX[j] != 0, "Column divisor cannot be zero");
        }

        for (uint256 i = 0; i < N; i++) {
            for (uint256 j = 0; j < N; j++) {
                matrixA[i][j] = (matrixZ[i][j] * SCALE_1) / vectorX[j];
            }
        }

        lastTCM = matrixA;
        emit TCMCalculated(matrixA);

        // LIM
        matrixL = _identity();
        {
            uint256[20][20] memory P = matrixA;
            _addInPlace(matrixL, P);

            for (uint256 k = 2; k <= K; k++) {
                P = _mulFixed(P, matrixA);
                _addInPlace(matrixL, P);
            }
        }

        lastLIM = matrixL;
        emit LIMUpdated(matrixL);

        // DIM
        for (uint256 i = 0; i < N; i++) {
            require(vectorX[i] != 0, "DIM divisor cannot be zero");
            matrixDIM[i] = (matrixE[i] * SCALE_1) / vectorX[i];
        }

        lastDIM = matrixDIM;
        emit DIMCalculated(matrixDIM);

        // TIM
        for (uint256 i = 0; i < N; i++) {
            for (uint256 j = 0; j < N; j++) {
                matrixT[i][j] = (matrixDIM[i] * matrixL[i][j]) / SCALE_2;
            }
        }

        lastTIM = matrixT;
        emit TIMCalculated(matrixT);

        // Production-based
        for (uint256 i = 0; i < N; i++) {
            for (uint256 j = 0; j < N; j++) {
                matrixPB[i][j] = (matrixDIM[i] * matrixY[i][j]) / SCALE_1;
            }
        }

        lastProductionImpact = matrixPB;
        emit Production_basedImpactCalculated(matrixPB);

        // Consumption-based
        for (uint256 i = 0; i < N; i++) {
            for (uint256 j = 0; j < N; j++) {
                uint256 sum = 0;
                for (uint256 k = 0; k < N; k++) {
                    sum += (matrixT[i][k] * matrixY[k][j]) / SCALE_2;
                }
                matrixCB[i][j] = sum;
            }
        }

        lastConsumptionImpact = matrixCB;
        emit Consumption_basedImpactCalculated(matrixCB);

        return (matrixA, matrixL, matrixDIM, matrixT, matrixPB, matrixCB);
    }

    /*
        ------------------------------------------------------------
        Internal Helpers
        ------------------------------------------------------------
    */
    function _identity()
        internal
        pure
        returns (uint256[20][20] memory I)
    {
        for (uint256 i = 0; i < N; i++) {
            I[i][i] = SCALE_1;
        }
    }

    function _addInPlace(
        uint256[20][20] memory X,
        uint256[20][20] memory Y
    )
        internal
        pure
    {
        for (uint256 i = 0; i < N; i++) {
            for (uint256 j = 0; j < N; j++) {
                X[i][j] += Y[i][j];
            }
        }
    }

    function _mulFixed(
        uint256[20][20] memory A,
        uint256[20][20] memory B
    )
        internal
        pure
        returns (uint256[20][20] memory C)
    {
        for (uint256 i = 0; i < N; i++) {
            for (uint256 k = 0; k < N; k++) {
                uint256 aik = A[i][k];
                if (aik == 0) continue;

                for (uint256 j = 0; j < N; j++) {
                    C[i][j] += (aik * B[k][j]) / SCALE_2;
                }
            }
        }
    }
}
