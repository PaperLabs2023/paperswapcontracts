# contracts

interface IAMM {

    function addLiquidity(address _token0, address _token1, uint _amount0,uint _amount1) external  returns (uint shares);
    
    function addLiquidityWithETH(address _token, uint _tokenAmount) external  payable;
    
    function removeLiquidity(
        address _token0,
        address _token1,
        uint _shares
    ) external returns (uint amount0, uint amount1);

    //swap with sli parm _disirSli(parm): 万分之 parm
    function swapByLimitSli(address _tokenIn, address _tokenOut, uint _amountIn, uint _disirSli) external  returns(uint amountOut);
    //换取eth
    function swapToETH(address _tokenIn, uint _amountIn, uint _disirSli) external ;
    //用eth换token
    function swapWithETH(address _tokenOut,uint _disirSli) external  payable;

    function getReserve(address _lpTokenAddr, address _tokenAddr) external  view returns(uint);
}

# 新合约地址

### weth：0xD3BEC1c13A49BE9f29c8eE19090181Aec25D1404

### paperswap：0x5d49B0BA0CDe9878ec24F5c01527B2EcAA826613
#### 619更新address：0x7F68F598D10f63EcCcD5A92FA04c3916c9D6EE13

### Data：0xD96d3141170781eD16379D5EaDa5E452901B7323
#### 619更新address：0xBe7c34a4B9960911e3C817e81bC83eda522C5023

### FarmFactory：0x95De4f17fCf3bCeaa6E51c3243507A0F87F58c99
