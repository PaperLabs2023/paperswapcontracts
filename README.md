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
