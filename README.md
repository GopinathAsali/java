package com.Call;
import java.net.URL;
import java.net.MalformedURLException;	
import javax.xml.namespace.QName;
import javax.xml.ws.Service;
public class CustomerCall {
public static void main(String args[])throws MalformedURLException
{
	URL url=new URL("http://localhost:8080/Call?wsdl");
	QName qname=new QName("http://Call.com/","calculatorImpService");
	Service service=Service.create(url,qname);
calculator calservice=service.getPort(calculator.class);
System.out.println(calservice.add(12, 25));
}
}
