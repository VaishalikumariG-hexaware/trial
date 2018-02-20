@Test
    public void testApplyLeave() throws AssertionError, URISyntaxException {

        
     String res=given().accept(ContentType.JSON).contentType("application/json").body("{\"noOfDays\":\"1\",\"startDate\":\"2029-05-10\",\"endDate\":\"2029-05-10\",\"leaveReason\":\"sick\",\"empId\":\"3000\"}").
        when().post(CommonUtil.getURI("/api/employees/applyforleave")).getBody().asString();

	assertEquals("Application Status : Successfully applied for leave!",res);
	System.out.println("Result from Post Method  " +res + " Ramya");
