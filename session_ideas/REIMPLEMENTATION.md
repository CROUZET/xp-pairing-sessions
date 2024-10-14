# REIMPLEMENTATION

Take a standard function and do the implem from scratch

Participants in 2 to 3

## How

- Monkey patch as side function

# Example for Integer.sum 
# 4 custom implementations over 2 forms + tests + benchmark

```ruby
# exec example:
# - ruby /Users/henri.crouzet/RubymineProjects/sandbox/sandbox.rb
# - rspec /Users/henri.crouzet/RubymineProjects/sandbox/sandbox.rb
class Array
  def sum_using_inject
    return self.inject(0) { |sum,n| sum + yield(n) } if block_given?
    self.inject(:+)
  end

  def sum_using_reduce
    return self.reduce(0) { |sum,n| sum + yield(n) } if block_given?
    self.reduce(:+)
  end

  def sum_using_each
    total = 0
    self.each { |n| total += block_given? ? yield(n) : n }
    total
  end

  def sum_using_eval
    return eval(self.map { |n| yield(n) }*?+) if block_given?
    eval(self*?+)
  end
end

if __FILE__ == $0
  require 'benchmark'

  tested = (-6..45).to_a
  TIMES = 100_000
  procs = Proc.new { |n| n.abs.digits.size }

  Benchmark.bm(7) do |x|
    x.report("CLASSIC") { TIMES.times { tested.sum + tested.sum(&procs) } }
    x.report("_inject_") { TIMES.times { tested.sum_using_inject + tested.sum_using_inject(&procs) } }
    x.report("_reduce_") { TIMES.times { tested.sum_using_reduce + tested.sum_using_reduce(&procs) } }
    x.report("_each_") { TIMES.times { tested.sum_using_each + tested.sum_using_each(&procs) } }
    x.report("_eval_") { TIMES.times { tested.sum_using_eval + tested.sum_using_eval(&procs) } }
  end
end

if $0.split('/').last == 'rspec'
  require 'rspec'

  describe Array do
    let(:customs) { %i[sum_using_inject sum_using_each sum_using_reduce sum_using_eval] }
    let(:under_tests) { (-6..9).to_a }

    describe 'custom functions' do
      it 'works as the classic function - form 1' do
        customs.each { |custom| expect(under_tests.sum).to be_eql(under_tests.send(custom)) }
      end
      it 'works as the classic function - form 2' do
        procs = Proc.new { |n| n.abs.digits.size }
        customs.each { |custom| expect(under_tests.sum(&procs)).to be_eql(under_tests.send(custom, &procs)) }
      end
    end
  end
end
```

## Refactoring Examples

- Integer.times
- String.rjust
- Enumerable.count

## To go further

- contribute on ruby core ? :D
