###equals, hashCode 상속 lib로 간단히
####[Java 의 equlas 과 hashCode, 동등성과 동일성](http://anster.tistory.com/160)
	@Override
	public boolean equals(Object obj) {
	    if (obj == this) {
	        return true;
	    }
	    if (!(obj instanceof Type)) {
	        return false;
	    }
	    Type type = (Type) obj;
	
	    return new EqualsBuilder()
	            .append(this.1, type.1)
	            .isEquals();
	}
	
	@Override
	public int hashCode() {
	    return Objects.hash(~);
	}
